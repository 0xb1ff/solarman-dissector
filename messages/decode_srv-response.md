# server response message
##### [back to readme](../README.md)  
V5 table

message type 0x1110 (hello response), 0x1210 (data response), 0x1710 (keep alive response), 0x1810 (hello end response)

77 bytes on wire

23 bytes SolarmanV5 data   

| HEX  	| DEC 	| TYPE     	| VALUE                                                                                                     	|
|------	|-----:	|----------	|--------------------------------------------------------------------------------------------------------------	|
| 0x00 	| 0   	| uInt8    	| always 0xa5                                                                                                	|
| 0x01 	| 1   	| uInt16LE 	| msg length - always 10, excl msg header(0x00 - 0x0A), checksum and last byte                               	|
| 0x02 	| 2   	| "       	| msg length - always 00                                                                                     	|
| 0x03 	| 3   	| uInt16LE 	| msg type - always 0x10                                                                                    	|
| 0x04 	| 4   	| "       	| msg type - 0x11: hello response, 0x12: data response, 0x17: keep alive rsp, 0x18: hello end rsp            	|
| 0x05 	| 5   	| uInt8    	| server message serial nr - starts from 00 (synced with server)                                             	|
| 0x06 	| 6   	| uInt8    	| unit message serial nr - starts from 01                                                                   	|
| 0x07 	| 7   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x08 	| 8   	| "       	| data logger SN (Embedded Device SN)                                                                        	|
| 0x09 	| 9   	| "       	| data logger SN (Embedded Device SN)                                                                        	|
| 0x0A 	| 10  	| "       	| data logger SN (Embedded Device SN)                                                                        	|
| ---- 	| --- 	| -------- 	|                                                                                                           	|
| 0x0B 	| 11  	| uInt8    	| frame type - 00: keep alive, 01: data logger (data rsp, hello end rsp), 02: solar inverter (hello rsp)      |
| 0x0C 	| 12  	| uInt8   	| status - 0x01: OK                                                                              	            |
| 0x0D 	| 13  	| uInt32LE 	| unix time stamp                                                                                         	  |
| 0x0E 	| 14  	| "       	| unix time stamp                                                                                         	  |
| 0x0F 	| 15  	| "        	| unix time stamp                                                                                         	  |
| 0x10 	| 16  	| "        	| unix time stamp                                                                                         	  |
| 0x11 	| 17  	| uInt8 	  | heart rate, always 120 (seconds)                                                                          	|  
| 0x12 	| 11  	| uInt8    	| always 00                                                                                                   |
| 0x13 	| 11  	| uInt8    	| always 00                                                                                                   |
| 0x14 	| 11  	| uInt8    	| always 00                                                                                                   |
| 0x15 	| 18  	| uInt8    	| checksum - add all bytes, except first, last, and checksum itself, then mod 256                           	|
| 0x16 	| 19  	| uInt8    	| always 0x15                                                                                                	|
