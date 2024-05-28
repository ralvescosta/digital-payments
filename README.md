# ISO 8583 Sample Message

08002038000000200002810000000001084909052253415630305A303537363331202020205341564E47583130303131303032303030302020202020200011010008B9F3F723CA3CD2F8

## Breaking this message dawn we've got

- MTI = 0800

- Bitmap = 2038000000200002

- Data Fields = 810000000001084909052253415630305A303537363331202020205341564E47583130303131303032303030302020202020200011010008B9F3F723CA3CD2F8


### MTI - Message type indicator

- 0 - ISO 8583 Version - in this case: 0
- 8 - Message class ---- in this case: Network management message
- 0 - Message function - in this case: Request from acquirer to issuer to carry out an action; issuer may accept or reject
- 0 - Message origin --- in this case: Acquirer

### BitMap

- 20 - 00100000 -> bit 3

- 38 - 00111000 -> bits 11, 12, 13

- 00 - 00000000

- 00 - 00000000

- 00 - 00000000

- 20 - 00100000 -> bit 43

- 00 - 00000000

- 02 - 00000010 -> bit 63

### Data Filed

Now as we already now each bit wi will have in the message, we just need to follow the ISO documentation que retrieve each bit in the message

#### Bit 3 - Processing code n6
= *810000*

#### Bit 11 - System trace audit number (STAN) n6
= *000001*

#### Bit 12 - Local transaction date (MMDD) n6
= *084909*

#### Bit 13 - Local transaction date (MMDD) n4
= *0522*

#### Bit 43 - Card acceptor name/location (1–25 card acceptor name or automated teller machine (ATM) location, 26-28 city name, 39-40 country code) n40
= *53415630305A303537363331202020205341564E4758313030313130303230303030202020202020*

#### Bit 63 - Reserved (private) 0...999
= *0011010008B9F3F723CA3CD2F8*




## Dynamic Key Exchange


- https://www.linkedin.com/pulse/card-payments-iso-8583-dynamic-key-exchange-pin-encryption-kumar/