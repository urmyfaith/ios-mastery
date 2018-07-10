# [MultipeerConnectivity](https://developer.apple.com/documentation/multipeerconnectivity)

## Phases

- [discovery](discovery.md)
  - [discovery-plus](discovery-plus.md)
- [session](session.md)

## API 

Category|Class|Protocol
---|---|---
server|[MCNearbyServiceAdvertiser](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyserviceadvertiser)|[MCNearbyServiceAdvertiserDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyserviceadvertiserdelegate)
client|[MCNearbyServiceBrowser](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyservicebrowser)|[MCNearbyServiceBrowserDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyservicebrowserdelegate)
server-plus|[MCAdvertiserAssistant](https://developer.apple.com/documentation/multipeerconnectivity/mcadvertiserassistant)|[MCAdvertiserAssistantDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcadvertiserassistantdelegate)
client-plus|[MCBrowserViewController](https://developer.apple.com/documentation/multipeerconnectivity/mcbrowserviewcontroller)|[MCBrowserViewControllerDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcbrowserviewcontrollerdelegate)
session|[MCSession](https://developer.apple.com/documentation/multipeerconnectivity/mcsession)|[MCSessionDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcsessiondelegate)
model|[MCPeerID](https://developer.apple.com/documentation/multipeerconnectivity/mcpeerid)


## [MCPeerID](https://developer.apple.com/documentation/multipeerconnectivity/mcpeerid)


init(displayName myDisplayName: String)

var displayName: String { get }
