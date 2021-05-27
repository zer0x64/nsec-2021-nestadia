# Nestadia NSEC 2021 snapshot
![Logo](images/logo-nestadia-background.png)

## What is Nestadia?
Nestadia is a NES emulator written for NorthSec CTF 2021. The emulator ran as a "cloud gaming platform", AKA the actual emulator ran on a server and video and controller were streamed between the client and the server.  
The contestants had to reverse engineer the emulator to leak a "game prototype" and exploit a backdoor in the emulator to leak the flags. At the very end, the contestants were required to exploit an Arbitrary Code Execution vulnerability in the game prototype to get the last flag.  
**This snapshot of the repo was made for a cybersecurity competition and contains a backdoor and code specific to that competition. A cleaned and current version of the emulator can be found [here!](https://github.com/zer0x64/nestadia)**

## How to build and run.
### Client
First you need to build the client and place it where nestadia-server can find it:
```
cd nestadia-client
npm run build
cp -r ./dist ../nestadia-server/client_build/
```

### Server
You then need to build and run the server:
```
cd nestadia-server
cargo run --release
```

## License
Code is provided under the MIT or Apache license.
