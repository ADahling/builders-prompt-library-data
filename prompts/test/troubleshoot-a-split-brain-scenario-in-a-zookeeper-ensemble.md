---
title: "Troubleshoot a Split-Brain Scenario in a ZooKeeper Ensemble"
slug: troubleshoot-a-split-brain-scenario-in-a-zookeeper-ensemble
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/troubleshoot-a-split-brain-scenario-in-a-zookeeper-ensemble
---
# Troubleshoot a Split-Brain Scenario in a ZooKeeper Ensemble

Diagnose and resolve ZooKeeper split-brain partitions by verifying node status and restoring quorum integrity through state synchronization.

## Prompt

You are a distributed systems operator. Your Apache ZooKeeper ensemble, which is used for service discovery and leader election in your distributed system, is behaving erratically. You suspect a network partition has caused a split-brain scenario, where multiple nodes believe they are the leader. Your task is to diagnose and recover from this state.

Context:
- The ZooKeeper ensemble has 5 nodes.
- A network issue has partitioned the cluster into a group of 3 nodes and a group of 2 nodes.
- The group of 3 has a quorum and has elected a leader. The group of 2 does not have a quorum but may be serving stale data to clients connected to it.

Provide:
1. An explanation of how ZooKeeper’s quorum-based leader election works and how it is designed to prevent split-brain.
2. A set of commands using the ZooKeeper four-letter words (like `stat`, `ruok`, `srvr`) to check the status of each node and determine which ones are part of the majority quorum and who the leader is.
3. A recovery plan that involves fixing the network partition and ensuring that the nodes in the minority partition rejoin the main ensemble and sync their state from the leader.

## Tips

A highly specific and advanced troubleshooting scenario for a critical piece of distributed infrastructure.
