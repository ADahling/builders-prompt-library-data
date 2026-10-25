---
title: "OpenClaw: gRPC Service Design Guide"
slug: openclaw-grpc-service-design-guide
stage: Build
category: "OpenClaw"
grade: C
score: 62
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-grpc-service-design-guide
---
# OpenClaw: gRPC Service Design Guide

Get gRPC service design guidance with proto examples, message rules, pagination patterns, and error handling for service APIs.

## Prompt

# gRPC Service Design Guide

## Proto File Best Practices

### Service Definition
```protobuf
syntax = "proto3";
package company.service.v1;

// Use versioned packages
option go_package = "github.com/company/service/v1";

service OrderService {
  // Use verb-noun naming for RPCs
  rpc CreateOrder (CreateOrderRequest) returns (CreateOrderResponse);
  rpc GetOrder (GetOrderRequest) returns (Order);
  rpc ListOrders (ListOrdersRequest) returns (ListOrdersResponse);
  rpc UpdateOrder (UpdateOrderRequest) returns (Order);
  rpc DeleteOrder (DeleteOrderRequest) returns (google.protobuf.Empty);
  
  // Streaming RPCs
  rpc WatchOrders (WatchOrdersRequest) returns (stream OrderEvent);
}
```

### Message Design Rules
- Every RPC gets its own Request/Response message (even if similar)
- Use `google.protobuf.FieldMask` for partial updates
- Use `google.protobuf.Timestamp` for times (not int64)
- Reserve field numbers when removing fields (never reuse)
- Use wrapper types for nullable scalars (`google.protobuf.StringValue`)

### Pagination
```protobuf
message ListOrdersRequest {
  int32 page_size = 1;       // max items per page
  string page_token = 2;     // opaque cursor
  string filter = 3;         // AIP-160 filter syntax
  string order_by = 4;       // "created_at desc"
}

message ListOrdersResponse {
  repeated Order orders = 1;
  string next_page_token = 2;
  int32 total_size = 3;
}
```

## Error Handling
| gRPC Code | HTTP Equivalent | Use For |
|-----------|----------------|---------|
| OK | 200 | Success |
| INVALID_ARGUMENT | 400 | Validation errors |
| NOT_FOUND | 404 | Resource doesn't exist |
| ALREADY_EXISTS | 409 | Duplicate creation |
| PERMISSION_DENIED | 403 | Authorization failure |
| UNAUTHENTICATED | 401 | Missing/invalid credentials |
| RESOURCE_EXHAUSTED | 429 | Rate limited |
| INTERNAL | 500 | Unexpected server error |
| UNAVAILABLE | 503 | Service temporarily down |
| DEADLINE_EXCEEDED | 504 | Timeout |

## Production Checklist
- [ ] Deadlines set on every RPC call (no unbounded requests)
- [ ] Interceptors for: logging, auth, metrics, tracing
- [ ] Health check service (gRPC Health Checking Protocol)
- [ ] Reflection enabled in dev, disabled in production
- [ ] Load balancing: client-side (preferred) or proxy-based
- [ ] Keepalive configured to detect dead connections
- [ ] Max message size explicitly configured

## Tips

gRPC service design guide covering proto file best practices, message design, pagination, error handling, and production checklist.
