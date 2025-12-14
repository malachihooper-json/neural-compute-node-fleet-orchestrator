# Orchestrator Core

Plug-and-play distributed system coordinator for compute node fleets.

## Quick Start

```bash
dotnet build
```

```csharp
using OrchestratorCore;

var orchestrator = new OrchestratorService();
await orchestrator.StartAsync();
var nodes = await orchestrator.GetRegisteredNodesAsync();
await orchestrator.DistributeWorkAsync(workItems);
```

## Components

| File | Purpose |
|------|---------|
| ShardCoordinator.cs | Shard allocation across nodes |
| DroneRegistry.cs | Fleet management with health monitoring |
| OrchestratorService.cs | Main service implementation |
| CellularCoordinator.cs | Cellular resource coordination |
| VersionManager.cs | Deployment versioning |
| PromptQueue.cs | Work queue distribution |
| LedgerService.cs | Distributed transaction ledger |
| BackgroundServices.cs | Background task runners |
| FormationSuite.cs | Node formation patterns |

## Features

- Centralized node registration and discovery
- Work distribution with load balancing
- Version-controlled deployments
- Health monitoring and automatic failover
- Distributed audit ledger

## Requirements

- .NET 8.0+
- Network access for node communication
