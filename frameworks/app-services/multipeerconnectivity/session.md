


## [MCSession](https://developer.apple.com/documentation/multipeerconnectivity/mcsession)

convenience init(peer myPeerID: MCPeerID)

init(peer myPeerID: MCPeerID, 
securityIdentity identity: [Any]?, 
encryptionPreference: MCEncryptionPreference)

weak var delegate: MCSessionDelegate? { get set }

var encryptionPreference: MCEncryptionPreference { get }

var myPeerID: MCPeerID { get }

var securityIdentity: [Any]? { get }

### Managing Peers Manually

func connectPeer(_ peerID: MCPeerID, 
withNearbyConnectionData data: Data)

func cancelConnectPeer(_ peerID: MCPeerID)

var connectedPeers: [MCPeerID] { get }

func nearbyConnectionData(forPeer peerID: MCPeerID, 
    withCompletionHandler completionHandler: @escaping (Data?, Error?) -> Void)

### Sending Data and Resources

func send(_ data: Data, 
  toPeers peerIDs: [MCPeerID], 
     with mode: MCSessionSendDataMode) throws

func sendResource(at resourceURL: URL, 
         withName resourceName: String, 
           toPeer peerID: MCPeerID, 
withCompletionHandler completionHandler: ((Error?) -> Void)? = nil) -> Progress?

func startStream(withName streamName: String, 
          toPeer peerID: MCPeerID) throws -> OutputStream

func disconnect()


### [enum MCSessionSendDataMode](https://developer.apple.com/documentation/multipeerconnectivity/mcsessionsenddatamode)


### [enum MCSessionState](https://developer.apple.com/documentation/multipeerconnectivity/mcsessionstate)


### [MCEncryptionPreference](https://developer.apple.com/documentation/multipeerconnectivity/mcencryptionpreference)

### [MCError.Code](https://developer.apple.com/documentation/multipeerconnectivity/mcerror/code)

## [MCSessionDelegate](https://developer.apple.com/documentation/multipeerconnectivity/mcsessiondelegate)


func session(_ session: MCSession, 
  didReceive data: Data, 
    fromPeer peerID: MCPeerID)

func session(_ session: MCSession, 
didStartReceivingResourceWithName resourceName: String, 
    fromPeer peerID: MCPeerID, 
        with progress: Progress)


didFinishReceivingResourceWithName resourceName: String, 
    fromPeer peerID: MCPeerID, 
          at localURL: URL?, 
   withError error: Error?)


func session(_ session: MCSession, 
  didReceive stream: InputStream, 
    withName streamName: String, 
    fromPeer peerID: MCPeerID)


func session(_ session: MCSession, 
        peer peerID: MCPeerID, 
   didChange state: MCSessionState)


didReceiveCertificate certificate: [Any]?, 
             fromPeer peerID: MCPeerID, 
   certificateHandler: @escaping (Bool) -> Void)
