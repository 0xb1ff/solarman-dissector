# hello end message
##### [back to readme](../README.md)  
V5 table

message type 0x4810

127 bytes on wire

73 bytes SolarmanV5 data   

| HEX  	| DEC 	| TYPE     	| VALUE                                                                                                     	|
|------	|-----:	|----------	|--------------------------------------------------------------------------------------------------------------	|
| 0x00 	| 0   	| uInt8    	| always a5                                                                                                 	|
| 0x01 	| 1   	| uInt16LE 	| always 60 msg length - excl msg header(0x00 - 0x0A), checksum and last byte                               	|
| 0x02 	| 2   	| uInt16LE 	| always 00 msg length                                                                                      	|
| 0x03 	| 3   	| uInt16LE 	| always 10 msg type - hello end msg                                                                         	|
| 0x04 	| 4   	| uInt16LE 	| always 48 msg type - hello end msg                                                                         	|
| 0x05 	| 5   	| uInt8    	| server message serial nr - starts from 00 (synced with server)                                             	|
| 0x06 	| 6   	| uInt8    	| inverter message serial nr - starts from 01                                                                	|
| 0x07 	| 7   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x08 	| 8   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x09 	| 9   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x0A 	| 10  	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| ---- 	| --- 	| -------- 	|                                                                                                           	|
| 0x0B 	| 11  	| uInt8    	| always 01                                                                                                 	|
| 0x0C 	| 12  	| uInt32LE 	| uptime (sec)                                                                                              	|
| 0x0D 	| 13  	| "       	| uptime (sec)                                                                                              	|
| 0x0E 	| 14  	| "       	| uptime (sec)                                                                                              	|
| 0x0F 	| 15  	| "       	| uptime (sec)                                                                                              	|
| 0x10 	| 16  	| uInt32LE 	| timer - every >= 5240 s - reset after ~5240 seconds (1.5 h interval?),                                     	|
| 0x11 	| 17  	| "       	| timer - every >= 5240 s - communication restarts with hello_msg                                           	|
| 0x12 	| 18  	| "       	| timer - every >= 5240 s                                                                                    	|
| 0x13 	| 19  	| "       	| timer - every >= 5240 s                                                                                    	|
| 0x14 	| 20  	| uInt32LE 	| offset time                                                                                                	|
| 0x15 	| 21  	| "       	| offset time                                                                                                	|
| 0x16 	| 22  	| "       	| offset time                                                                                                	|
| 0x17 	| 23  	| "       	| offset time                                                                                                	|
| 0x18 	| 24    |	uInt8 	  | status - 0x01: OK                                                                                         	|
| ---- 	| --- 	| -------- 	|                                                                                                            	|
| 0x19 	| 25  	| uInt8    	| checksum - add all bytes, except first, last, and checksum itself, then mod 256                           	|
| 0x2A 	| 26  	| uInt8    	| always 0x15                                                                                                	|
