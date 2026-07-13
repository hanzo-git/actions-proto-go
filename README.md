# actions-proto-go

The wire protocol for **Hanzo Git Actions** — the protobuf /
[connect](https://connectrpc.com) contract spoken between the Hanzo Git runner
(`git-runner`) and the Hanzo Git server at `git.hanzo.ai`.

Two services:

- `runner.v1.RunnerService` — runner registration, task fetch, task/log updates.
- `ping.v1.PingService` — health / liveness ping.

## Use

```go
import (
	runnerv1 "github.com/hanzo-git/actions-proto-go/runner/v1"
	"github.com/hanzo-git/actions-proto-go/runner/v1/runnerv1connect"
)
```

## Provenance

Derived work; upstream attribution and MIT license terms are in `NOTICE` and
`LICENSE`. The on-the-wire protobuf identities (`runner.v1.*`, `ping.v1.*`) are
unchanged, so it stays protocol-compatible with the server.
