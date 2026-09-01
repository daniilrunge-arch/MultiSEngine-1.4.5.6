# MultiSEngine 1.2.0.8 — Terraria 1.4.5.6

## Critical fix

Client stayed on "Requesting tile data" because after switch the proxy never sent
`StartPlaying` + `FinishedConnectingToServer` to the **client**.

Server tiles were already flowing; client just never left the loading screen.

### Now FinishedConnectingAsync always sends:
1. StartPlaying
2. FinishedConnectingToServer

## lib/
- TrProtocol.dll — compatible runtime DLL (required)
- TrProtocol.1.4.5.6.dll — new protocol (290KB) for future port — do NOT replace blindly

## Run
```bat
cd MultiSEngine
dotnet run -c Release
```
