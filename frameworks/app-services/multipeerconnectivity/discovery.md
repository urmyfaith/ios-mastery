

[MCNearbyServiceAdvertiser](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyserviceadvertiser)|[MCNearbyServiceAdvertiserDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyserviceadvertiserdelegate)



## [MCNearbyServiceBrowser](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyservicebrowser)|

init(peer myPeerID: MCPeerID, 
serviceType: String)

weak var delegate: MCNearbyServiceBrowserDelegate? { get set }

var myPeerID: MCPeerID { get }

var serviceType: String { get }

func startBrowsingForPeers()

func stopBrowsingForPeers()

func invitePeer(_ peerID: MCPeerID, 
             to session: MCSession, 
    withContext context: Data?, 
        timeout: TimeInterval)



## [MCNearbyServiceBrowserDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyservicebrowserdelegate)


optional func browser(_ browser: MCNearbyServiceBrowser, 
didNotStartBrowsingForPeers error: Error)

func browser(_ browser: MCNearbyServiceBrowser, 
   foundPeer peerID: MCPeerID, 
withDiscoveryInfo info: [String : String]?)

func browser(_ browser: MCNearbyServiceBrowser, 
    lostPeer peerID: MCPeerID)