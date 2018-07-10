

## [MCNearbyServiceAdvertiser](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyserviceadvertiser)

init(peer myPeerID: MCPeerID, 
discoveryInfo info: [String : String]?, 
serviceType: String)

weak var delegate: MCNearbyServiceAdvertiserDelegate? { get set }

var discoveryInfo: [String : String]? { get }

var myPeerID: MCPeerID { get }

var serviceType: String { get }

func startAdvertisingPeer()

func stopAdvertisingPeer()



## [MCNearbyServiceAdvertiserDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcnearbyserviceadvertiserdelegate)

optional func advertiser(_ advertiser: MCNearbyServiceAdvertiser, 
didNotStartAdvertisingPeer error: Error)

func advertiser(_ advertiser: MCNearbyServiceAdvertiser, 
didReceiveInvitationFromPeer peerID: MCPeerID, 
    withContext context: Data?, 
invitationHandler: @escaping (Bool, MCSession?) -> Void)

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