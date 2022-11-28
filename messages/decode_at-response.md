# unit AT response message
##### [back to readme](../README.md)  
V5 table

message type 0x1510

message size depends on payload   

| HEX  	| DEC 	| TYPE     	| VALUE                                                                                                     	|
|------	|-----:	|----------	|--------------------------------------------------------------------------------------------------------------	|
| 0x00 	| 0   	| uInt8    	| always a5                                                                                                 	|
| 0x01 	| 1   	| uInt16LE 	| msg length - excl msg header(0x00 - 0x0A), checksum and last byte                                         	|
| 0x02 	| 2   	| "       	| msg length                                                                                                	|
| 0x03 	| 3   	| uInt16LE 	| always 10 msg type - AT response msg                                                                      	|
| 0x04 	| 4   	| "       	| always 15 msg type - AT response msg                                                                      	|
| 0x05 	| 5   	| uInt8    	| server message serial nr - starts from 01 (synced with server)                                             	|
| 0x06 	| 6   	| uInt8    	| unit message serial nr - starts from 01                                                                   	|
| 0x07 	| 7   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x08 	| 8   	| "       	| data logger SN (Embedded Device SN)                                                                        	|
| 0x09 	| 9   	| "       	| data logger SN (Embedded Device SN)                                                                        	|
| 0x0A 	| 10  	| "       	| data logger SN (Embedded Device SN)                                                                        	|
| ---- 	| --- 	| -------- 	|                                                                                                           	|
| 0x0B 	| 11  	| uInt8    	| frame type - always 01 (data logger)                                                                       	|
| 0x0C 	| 12  	| uInt8   	| status - 0x01: OK                                                                              	            |
| 0x0D 	| 13  	| uInt32LE 	| uptime ?                                                                                                	  |
| 0x0E 	| 14  	| "       	| uptime ?                                                                                                	  |
| 0x0F 	| 15  	| "        	| uptime ?                                                                                                	  |
| 0x10 	| 16  	| "        	| uptime ?                                                                                                	  |
| 0x11 	| 17  	| uInt32LE 	| timer ?                                                                                                   	|
| 0x12 	| 18  	| "       	| timer ?                                                                                                   	|
| 0x13 	| 19  	| "       	| timer ?                                                                                                   	|
| 0x14 	| 20  	| "       	| timer ?                                                                                                   	|
| 0x15 	| 21  	| uInt32LE 	| offset time ?                                                                                              	|
| 0x16 	| 22  	| "       	| offset time ?                                                                                             	|
| 0x17 	| 23  	| "       	| offset time ?                                                                                              	|
| 0x18 	| 24  	| "       	| offset time ?                                                                                             	|
| 0x19 	| 25  	| string    | AT response, e.g. '+ok'                                                                                    	|
| ---- 	| --- 	| -------- 	|                                                                                                            	|
| 0x.. 	| ..  	| uInt8    	| checksum - add all bytes, except first, last, and checksum itself, then mod 256                           	|
| 0x.. 	| ..  	| uInt8    	| always 0x15                                                                                                	|

Source: https://www.photovoltaikforum.com/thread/179529-daten-von-deye-sun-mikrowechselrichtern-abfangen/?pageNo=3
