# hello message
##### [back to readme](../README.md)  
V5 table

message type 0x4110

197 bytes on wire

143 bytes SolarmanV5 data   

| HEX  	| DEC 	| TYPE     	| VALUE                                                                                                     	|
|------	|-----:	|----------	|--------------------------------------------------------------------------------------------------------------	|
| 0x00 	| 0   	| uInt8    	| always a5                                                                                                 	|
| 0x01 	| 1   	| uInt16LE 	| always 130 msg length - excl msg header(0x00 - 0x0A), checksum and last byte                               	|
| 0x02 	| 2   	| uInt16LE 	| always 00 msg length                                                                                      	|
| 0x03 	| 3   	| uInt16LE 	| always 10 msg type - hello msg                                                                            	|
| 0x04 	| 4   	| uInt16LE 	| always 41 msg type - hello msg                                                                            	|
| 0x05 	| 5   	| uInt8    	| server message serial nr - starts from 00 (synced with server)                                             	|
| 0x06 	| 6   	| uInt8    	| inverter message serial nr - starts from 01                                                                	|
| 0x07 	| 7   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x08 	| 8   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x09 	| 9   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x0A 	| 10  	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| ---- 	| --- 	| -------- 	|                                                                                                           	|
| 0x0B 	| 11  	| uInt8    	| always 01                                                                                                 	|
| 0x0C 	| 12  	| uInt32LE 	| total operation time (sec)                                                                                	|
| 0x0D 	| 13  	| uInt32LE 	| total operation time (sec)                                                                                	|
| 0x0E 	| 14  	| uInt32LE 	| total operation time (sec)                                                                                	|
| 0x0F 	| 15  	| uInt32LE 	| total operation time (sec)                                                                                	|
| 0x10 	| 16  	| uInt32LE 	| timer - every >= 5240 s - reset after ~5240 seconds (1.5 h interval?),                                     	|
| 0x11 	| 17  	| uInt32LE 	| timer - every >= 5240 s - communication restarts with hello_msg                                           	|
| 0x12 	| 18  	| uInt32LE 	| timer - every >= 5240 s                                                                                    	|
| 0x13 	| 19  	| uInt32LE 	| timer - every >= 5240 s                                                                                    	|
| 0x14 	| 20  	| uInt32LE 	| always 00                                                                                                 	|
| 0x15 	| 21  	| uInt32LE 	| always 00                                                                                                 	|
| 0x16 	| 22  	| uInt32LE 	| always 00                                                                                                 	|
| 0x17 	| 23  	| uInt32LE 	| always 00                                                                                                 	|
| 0x18 	| 24  	| uInt8    	| upload period, always 5 (minutes)                                                                          	|
| 0x19 	| 25  	| uInt8    	| data acquisition period, always 60 (seconds)                                                               	|
| 0x1A 	| 26  	| uInt8    	| heart rate, always 120 (seconds)                                                                           	|
| 0x1B 	| 27  	| uInt8    	| always 0x01 (max nr of connected devices or command type ?)                                               	|
| 0x1C 	| 28  	| uInt8    	| wifi signal strength                                                                                       	|
| 0x1D 	| 29  	| uInt8    	| always 0x01 (sensor type nr ?)                                                                             	|
| 0x1E 	| 30  	| string   	| module version - string (40 bytes, ASCII code, padded with 00)                                             	|
| 0x1F 	| 31  	| string   	| module version - string                                                                                   	|
| 0x20 	| 32  	| string   	| module version - string               I                                                                    	|
| 0x21 	| 33  	| string   	| module version - string                                                                                   	|
| 0x22 	| 34  	| string   	| module version - string                                                                                   	|
| 0x23 	| 35  	| string   	| module version - string                                                                                   	|
| 0x24 	| 36  	| string   	| module version - string                                                                                   	|
| 0x25 	| 37  	| string   	| module version - string                                                                                   	|
| 0x26 	| 38  	| string   	| module version - string                                                                                   	|
| 0x27 	| 39  	| string   	| module version - string                                                                                   	|
| 0x28 	| 40  	| string   	| module version - string                                                                                   	|
| 0x29 	| 41  	| string   	| module version - string                                                                                   	|
| 0x2A 	| 42  	| string   	| module version - string                                                                                   	|
| 0x2B 	| 43  	| string   	| module version - string                                                                                   	|
| 0x2C 	| 44  	| string   	| module version - string                                                                                   	|
| 0x2D 	| 45  	| string   	| module version - string                                                                                   	|
| 0x2E 	| 46  	| string   	| module version - string                                                                                   	|
| 0x2F 	| 47  	| string   	| module version - string                                                                                   	|
| 0x30 	| 48  	| string   	| module version - string                                                                                   	|
| 0x31 	| 49  	| string   	| module version - string                                                                                   	|
| 0x32 	| 50  	| string   	| module version - string                                                                                   	|
| 0x33 	| 51  	| string   	| module version - string                                                                                   	|
| 0x34 	| 52  	| string   	| module version - string                                                                                   	|
| 0x35 	| 53  	| string   	| module version - string                                                                                   	|
| 0x36 	| 54  	| string   	| module version - string                                                                                   	|
| 0x37 	| 55  	| string   	| module version - string                                                                                   	|
| 0x38 	| 56  	| string   	| module version - string                                                                                   	|
| 0x39 	| 57  	| string   	| module version - string                                                                                   	|
| 0x3A 	| 58  	| string   	| module version - string                                                                                   	|
| 0x3B 	| 59  	| string   	| module version - string                                                                                   	|
| 0x3C 	| 60  	| string   	| module version - string                                                                                   	|
| 0x3D 	| 61  	| string   	| module version - string                                                                                   	|
| 0x3E 	| 62  	| string   	| module version - string                                                                                   	|
| 0x3F 	| 63  	| string   	| module version - string                                                                                   	|
| 0x40 	| 64  	| string   	| module version - string                                                                                   	|
| 0x41 	| 65  	| string   	| module version - string                                                                                   	|
| 0x42 	| 66  	| string   	| module version - string                                                                                   	|
| 0x43 	| 67  	| string   	| module version - string                                                                                   	|
| 0x44 	| 68  	| string   	| module version - string                                                                                   	|
| 0x45 	| 69  	| string   	| module version - string                                                                                   	|
| 0x46 	| 70  	| hex      	| STA mac address (6)                                                                                       	|
| 0x47 	| 71  	| hex      	| STA mac address                                                                                           	|
| 0x48 	| 72  	| hex      	| STA mac address                                                                                           	|
| 0x49 	| 73  	| hex      	| STA mac address                                                                                           	|
| 0x4A 	| 74  	| hex      	| STA mac address                                                                                           	|
| 0x4B 	| 75  	| hex      	| STA mac address                                                                                           	|
| 0x4C 	| 76  	| string   	| local IP - string (16 bytes ?, ASCII coded, padded with 00 at end)                                         	|
| 0x4D 	| 77  	| string   	| local IP - string                                                                                         	|
| 0x4E 	| 78  	| string   	| local IP - string                                                                                          	|
| 0x4F 	| 79  	| string   	| local IP - string                                                                                         	|
| 0x50 	| 80  	| string   	| local IP - string                                                                                         	|
| 0x51 	| 81  	| string   	| local IP - string                                                                                         	|
| 0x52 	| 82  	| string   	| local IP - string                                                                                         	|
| 0x53 	| 83  	| string   	| local IP - string                                                                                         	|
| 0x54 	| 84  	| string   	| local IP - string                                                                                         	|
| 0x55 	| 85  	| string   	| local IP - string                                                                                         	|
| 0x56 	| 86  	| string   	| local IP - string                                                                                         	|
| 0x57 	| 87  	| string   	| local IP - string                                                                                         	|
| 0x58 	| 88  	| string   	| local IP - string                                                                                         	|
| 0x59 	| 89  	| string   	| local IP - string                                                                                         	|
| 0x5A 	| 90  	| string   	| local IP - string                                                                                         	|
| 0x5B 	| 91  	| string  	| local IP - string                                                                                          	|
| 0x5C 	| 92  	| uInt8   	| always 0x00                                                                                               	|
| 0x5D 	| 93  	| uInt8   	| always 0x00                                                                                                	|
| 0x5E 	| 94  	| uInt8   	| always 0x01                                                                                                	|
| 0x5F 	| 95  	| uInt8   	| always 0x06                                                                                                	|
| 0x60 	| 96  	| uInt8   	| always 0x54                                                                                                	|
| 0x61  | 97    | uInt8   	| always 0x07                                                                                                 |
| 0x62 	| 98  	| uInt8   	| always 0x00                                                                                                	|
| 0x63 	| 99  	| uInt8   	| always 0xFF (AT+ Update Command Supported ?)                                                               	|
| 0x64  | 100   | string   	| Extended System Version - string (40 bytes, ASCII code, padded with 00)                                    	|
| 0x65  | 101   | string   	| Extended System Version - string                                                                           	|
| 0x66  | 102   | string   	| Extended System Version - string      I                                                                    	|
| 0x67  | 103   | string   	| Extended System Version - string                                                                          	|
| 0x68  | 104   | string   	| Extended System Version - string                                                                           	|
| 0x69  | 105   | string   	| Extended System Version - string                                                                          	|
| 0x6A  | 106   | string   	| Extended System Version - string                                                                          	|
| 0x6B  | 107   | string   	| Extended System Version - string                                                                          	|
| 0x6C  | 108   | string   	| Extended System Version - string                                                                          	|
| 0x6D  | 109   | string   	| Extended System Version - string                                                                          	|
| 0x6E  | 110   | string   	| Extended System Version - string                                                                          	|
| 0x6F  | 111   | string   	| Extended System Version - string                                                                          	|
| 0x70  | 112   | string   	| Extended System Version - string                                                                          	|
| 0x71  | 113   | string   	| Extended System Version - string                                                                          	|
| 0x72  | 114   | string   	| Extended System Version - string                                                                          	|
| 0x73  | 115   | string   	| Extended System Version - string                                                                          	|
| 0x74  | 116   | string   	| Extended System Version - string                                                                          	|
| 0x75  | 117   | string   	| Extended System Version - string                                                                          	|
| 0x76  | 118   | string   	| Extended System Version - string                                                                          	|
| 0x77  | 119   | string   	| Extended System Version - string                                                                          	|
| 0x78  | 120   | string   	| Extended System Version - string                                                                          	|
| 0x79  | 121   | string   	| Extended System Version - string                                                                          	|
| 0x7A  | 122   | string   	| Extended System Version - string                                                                          	|
| 0x7B  | 123   | string   	| Extended System Version - string                                                                          	|
| 0x7C  | 124   | string   	| Extended System Version - string                                                                          	|
| 0x7D  | 125   | string   	| Extended System Version - string                                                                          	|
| 0x7E  | 126   | string   	| Extended System Version - string                                                                          	|
| 0x7F  | 127   | string   	| Extended System Version - string                                                                          	|
| 0x80  | 128   | string   	| Extended System Version - string                                                                          	|
| 0x81  | 129   | string   	| Extended System Version - string                                                                          	|
| 0x82  | 130   | string   	| Extended System Version - string                                                                          	|
| 0x83  | 131   | string   	| Extended System Version - string                                                                          	|
| 0x84  | 132   | string   	| Extended System Version - string                                                                          	|
| 0x85  | 133   | string   	| Extended System Version - string                                                                          	|
| 0x86  | 134   | string   	| Extended System Version - string                                                                          	|
| 0x87  | 135   | string   	| Extended System Version - string                                                                          	|
| 0x88  | 136   | string   	| Extended System Version - string                                                                          	|
| 0x89  | 137   | string   	| Extended System Version - string                                                                          	|
| 0x8A  | 138   | string   	| Extended System Version - string                                                                          	|
| 0x8B  | 139   | string   	| Extended System Version - string                                                                          	|
| 0x8C  | 140   | uInt8    	| always 0xFF (Protocol Upgrade Method ?)                                                                    	|
| ---- 	| --- 	| -------- 	|                                                                                                            	|
| 0x8D 	| 141  	| uInt8    	| checksum - add all bytes, except first, last, and checksum itself, then mod 256                           	|
| 0x8E 	| 143  	| uInt8    	| always 0x15                                                                                                	|
