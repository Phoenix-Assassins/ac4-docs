# NATTraversalProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | RequestProbeInitiation | [NATTraversalProtocol::RequestProbeInitiation_V1](#nattraversalprotocolrequestprobeinitiation_v1) |
| 2 | InitiateProbe | [NATTraversalProtocol::InitiateProbe_V1](#nattraversalprotocolinitiateprobe_v1) |
| 3 | RequestProbeInitiationExt | [NATTraversalProtocol::RequestProbeInitiationExt_V1](#nattraversalprotocolrequestprobeinitiationext_v1) |

# (1) RequestProbeInitiation

## NATTraversalProtocol::RequestProbeInitiation_V1

### Request

| Type | Name |
|------|------|
| qlist<stationurl> | urlTargetList |

### Response

This method does not return anything.

# (2) InitiateProbe

## NATTraversalProtocol::InitiateProbe_V1

### Request

| Type | Name |
|------|------|
| stationurl | urlStationToProbe |

### Response

This method does not return anything.

# (3) RequestProbeInitiationExt

## NATTraversalProtocol::RequestProbeInitiationExt_V1

### Request

| Type | Name |
|------|------|
| qlist<stationurl> | urlTargetList |
| stationurl | urlStationToProbe |

### Response

This method does not return anything.
