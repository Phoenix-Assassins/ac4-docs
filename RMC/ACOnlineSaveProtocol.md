# ACOnlineSaveProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | WriteSave | [ACOnlineSaveProtocol::WriteSave_V1](#aconlinesaveprotocolwritesave_v1) |
| 2 | ReadSave | [ACOnlineSaveProtocol::ReadSave_V1](#aconlinesaveprotocolreadsave_v1) |
| 3 | WriteWebSave | [ACOnlineSaveProtocol::WriteWebSave_V1](#aconlinesaveprotocolwritewebsave_v1) |
| 4 | ReadWebSave | [ACOnlineSaveProtocol::ReadWebSave_V1](#aconlinesaveprotocolreadwebsave_v1) |
| 5 | TestServerSideWriteSave | [ACOnlineSaveProtocol::TestServerSideWriteSave_V1](#aconlinesaveprotocoltestserversidewritesave_v1) |

# (1) WriteSave

## ACOnlineSaveProtocol::WriteSave_V1

### Request

| Type | Name |
|------|------|
| qBuffer | buffer |

### Response

This method does not return anything.

# (2) ReadSave

## ACOnlineSaveProtocol::ReadSave_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| bool | dataRetrieved |
| qBuffer | bufferOut |

# (3) WriteWebSave

## ACOnlineSaveProtocol::WriteWebSave_V1

### Request

| Type | Name |
|------|------|
| profileid | pid |
| string | buffer |

### Response

| Type | Name |
|------|------|
| bool | isSuccess |

# (4) ReadWebSave

## ACOnlineSaveProtocol::ReadWebSave_V1

### Request

| Type | Name |
|------|------|
| profileid | pid |

### Response

| Type | Name |
|------|------|
| string | buffer |

# (5) TestServerSideWriteSave

## ACOnlineSaveProtocol::TestServerSideWriteSave_V1

### Request

This method does not take any parameters.

### Response

This method does not return anything.
