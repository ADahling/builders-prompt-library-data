---
title: "Recover from Data Corruption in a RAID Array"
slug: recover-from-data-corruption-in-a-raid-array
stage: Test
category: "Critical Bugs"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/recover-from-data-corruption-in-a-raid-array
---
# Recover from Data Corruption in a RAID Array

Restore lost data from backups after a multi-disk RAID 5 failure and implement a more resilient storage architecture for future protection.

## Prompt

You are a system administrator. A server with a RAID 5 array has experienced a single disk failure. The array is now operating in a degraded state. While you were replacing the failed disk, a second disk in the same array failed. This has led to data loss, as a RAID 5 array can only tolerate a single disk failure. Your task is to recover as much data as possible.

Context:
- The server stores important file shares.
- You have nightly backups of the data to a separate backup server.
- The RAID controller is reporting that the array is offline.

Provide:
1. An explanation of why a RAID 5 array fails when two disks are lost.
2. A recovery plan that involves restoring the data from the last known good backup to a new, healthy storage volume. You will need to accept that any data changed between the last backup and the failure is lost.
3. A recommendation for a more resilient RAID level for this workload, such as RAID 6 (which can tolerate two disk failures) or RAID 10 (which offers better performance and can tolerate multiple disk failures in some cases).

## Tips

A classic data storage disaster recovery scenario.
