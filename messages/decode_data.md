# data message
##### [back to readme](../README.md)  
V5 table  
message type 0x4210    
602 bytes on wire    
547 bytes SolarmanV5 data  

| HEX  	| DEC 	| TYPE     	| VALUE                                                                                                     	|
|------	|-----:	|----------	|--------------------------------------------------------------------------------------------------------------	|
| 0x00 	| 0   	| uInt8    	| always 0xA5                                                                                                	|
| 0x01 	| 1   	| uInt16LE 	| always 0x16 msg length - 534 bytes excl msg header(0x00 - 0x0A), checksum and last byte                    	|
| 0x02 	| 2   	| uInt16LE 	| always 0x02 msg length                                                                                     	|
| 0x03 	| 3   	| uInt16LE 	| always 0x10 msg type - data                                                                                 	|
| 0x04 	| 4   	| uInt16LE 	| always 0x42 msg type - data                                                                                 	|
| 0x05 	| 5   	| uInt8    	| server message serial nr - copy of last server message serial nr received from server                      	|
| 0x06 	| 6   	| uInt8    	| inverter message serial nr - incremented from last inverter message serial nr sent to server               	|
| 0x07 	| 7   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x08 	| 8   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x09 	| 9   	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| 0x0A 	| 10  	| uInt32LE 	| data logger SN (Embedded Device SN)                                                                        	|
| ---- 	| --- 	| -------- 	|                                                                                                           	|
| 0x0B 	| 11  	| uInt8    	| always 0x01                                                                                               	|
| 0x0C 	| 12  	| uInt16LE 	| always 0x08 (Sensor Type)                                                                                 	|
| 0x0D 	| 13  	| uInt16LE 	| always 0x54 (Sensor Type)                                                                                 	|
| 0x0E 	| 14  	| uInt32LE 	| total operation time - in seconds                                                                          	|
| 0x0F 	| 15  	| uInt32LE 	| total operation time                                                                                      	|
| 0x10 	| 16  	| uInt32LE 	| total operation time                                                                                      	|
| 0x11 	| 17  	| uInt32LE 	| total operation time                                                                                      	|
| 0x12 	| 18  	| uInt32LE 	| timer - every >= 5240 s - reset after ~5240 seconds (1.5 h interval?),                                    	|
| 0x13 	| 19  	| uInt32LE 	| timer - every >= 5240 s - communication restarts with hello_msg                                           	|
| 0x14 	| 20  	| uInt32LE 	| timer - every >= 5240 s                                                                                   	|
| 0x15 	| 21  	| uInt32LE 	| timer - every >= 5240 s                                                                                    	|
| 0x16 	| 22  	| uInt32LE 	| offset time (Unix timestamp)                                                                               	|
| 0x17 	| 23  	| uInt32LE 	| offset time                                                                                               	|
| 0x18 	| 24  	| uInt32LE 	| offset time                                                                                               	|
| 0x19 	| 25  	| uInt32LE 	| offset time                                                                                               	|
| 0x1A 	| 26  	| uInt16LE 	| status (0x01 = OK)                                                                                         	|
| 0x1B 	| 27  	| uInt16LE 	| always 00                                                                                                 	|
| 0x1C 	| 28  	| uInt16LE 	| data message serial number, incremented with every msg, no reset - (uInt32LE?)                             	|
| 0x1D 	| 29  	| uInt16LE 	| data message serial number                                                                                	|
| 0x1E 	| 30  	| uInt16LE 	| always 00                                                                                                 	|
| 0x1F 	| 31  	| uInt16LE 	| always 00                                                                                                 	|
| 0x20 	| 32  	| string   	| inverter SN - string (10 bytes, ASCII coded)                                                               	|
| 0x21 	| 33  	| string   	| inverter SN - string                                                                                      	|
| 0x22 	| 34  	| string   	| inverter SN - string                                                                                      	|
| 0x23 	| 35  	| string   	| inverter SN - string                                                                                      	|
| 0x24 	| 36  	| string   	| inverter SN - string                                                                                      	|
| 0x25 	| 37  	| string   	| inverter SN - string                                                                                      	|
| 0x26 	| 38  	| string   	| inverter SN - string                                                                                      	|
| 0x27 	| 39  	| string   	| inverter SN - string                                                                                      	|
| 0x28 	| 40  	| string   	| inverter SN - string                                                                                      	|
| 0x29 	| 41  	| string   	| inverter SN - string                                                                                      	|
| 0x2A 	| 42  	| uInt8   	| always 0x04 ?                                                                                             	|
| 0x2B 	| 43  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x2C 	| 44  	| uInt32LE 	| daily energy in kWh/100                                                                                    	|
| 0x2D 	| 45  	| uInt32LE 	| daily energy in kWh/100                                                                                    	|
| 0x2E 	| 46  	| uInt32LE 	| daily energy in kWh/100                                                                                   	|
| 0x2F 	| 47  	| uInt32LE 	| daily energy in kWh/100                                                                              	      |
| 0x30 	| 48  	| uInt32LE  | total energy in kWh/100 - (uInt64LE ?)                                                                     	|
| 0x31 	| 49  	| uInt32LE 	| total energy in kWh/100                                                                                   	|
| 0x32 	| 50  	| uInt32LE 	| total energy in kWh/100                                                                                    	|
| 0x33 	| 51  	| uInt32LE 	| total energy in kWh/100                                                                                    	|
| 0x34 	| 52  	| uInt8   	| always 0x00 (?)                                                                                            	|
| 0x35 	| 53  	| uInt8 	  | always 0x00                                                                                               	|
| 0x36 	| 54  	| uInt8     | always 0x00                                                                                               	|
| 0x36 	| 55  	| uInt8   	| always 0x00                                                                                               	|
| 0x38 	| 56  	| uInt16LE 	| grid voltage in V/10                                                                                       	|
| 0x37 	| 57  	| uInt16LE 	| grid voltage in V/10                                                                                       	|
| 0x3A 	| 58  	| uInt8 	  | always 0x00                                                                                                	|
| 0x3B 	| 59  	| uInt8 	  | always 0x00                                                                                               	|
| 0x3C 	| 60  	| uInt8 	  | always 0x00                                                                                                	|
| 0x3D 	| 61  	| uInt8 	  | always 0x00                                                                                                	|
| 0x3E 	| 62  	| uInt8 	  | always 0x00                                                                                               	|
| 0x3F 	| 63  	| uInt8 	  | always 0x00                                                                                               	|
| 0x40 	| 64  	| uInt8 	  | always 0x00                                                                                               	|
| 0x41 	| 65  	| uInt8 	  | always 0x00                                                                                                	|
| 0x42 	| 66  	| uInt8 	  | always 0x00                                                                                               	|
| 0x43 	| 67  	| uInt8 	  | always 0x00                                                                                                	|
| 0x44 	| 68  	| uInt16LE 	| grid frequency in Hz/100                                                                                   	|
| 0x45 	| 79  	| uInt16LE 	| grid frequency in Hz/100                                                                                   	|
| 0x46 	| 70  	| uInt16LE 	| power to grid in W                                                                                         	|
| 0x47 	| 71  	| uInt16LE 	| power to grid in W                                                                                         	|
| 0x48 	| 72  	| uInt8 	  | always 0x00                                                                                               	|
| 0x49 	| 73  	| uInt8 	  | always 0x00                                                                                               	|
| 0x4A 	| 74  	| int16LE 	| heatsink temperature in °C/100 (signed!)                                                                   	|
| 0x4B 	| 75  	| int16LE 	| heatsink temperature in °C/100                                                                             	|
| 0x4C 	| 76  	| uInt8   	| always 0x18 ?                                                                                             	|
| 0x4D 	| 77  	| uInt8   	| always 0xFC ?                                                                                             	|
| 0x4E 	| 78  	| uInt8   	| always 0x18 ?                                                                                             	|
| 0x4F 	| 79  	| uInt8   	| always 0xFC ?                                                                                             	|
| 0x50 	| 80  	| uInt8   	| always 0x18 ?                                                                                             	|
| 0x51 	| 81  	| uInt8   	| always 0xFC ?                                                                                             	|
| 0x52 	| 82  	| uInt8   	| always 0x18 ?                                                                                             	|
| 0x53 	| 83  	| uInt8   	| always 0xFC ?                                                                                             	|
| 0x54 	| 84  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x55 	| 85  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x56 	| 86  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x57 	| 87  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x58 	| 88  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x59 	| 89  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x5A 	| 90  	| uInt8   	| always 0x00 ?                                                                                              	|
| 0x5B 	| 91  	| uInt8   	| always 0x00 ?                                                                                              	|
| 0x5C 	| 92  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x5D 	| 93  	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x5E 	| 94  	| uInt8   	| always 0x00 ?                                                                                              	|
| 0x5F 	| 95  	| uInt8   	| always 0x00 ?                                                                                              	|
| 0x60 	| 96  	| uInt16LE 	| VDC1 in V/10                                                                                               	|
| 0x61 	| 97  	| uInt16LE 	| VDC1 in V/10                                                                                              	|
| 0x62 	| 98  	| uInt16LE 	| IDC1 in A/10                                                                                              	|
| 0x63 	| 99  	| uInt16LE 	| IDC1 in A/10                                                                                              	|
| 0x64 	| 100 	| uInt16LE 	| VDC2 in V/10                                                                                              	|
| 0x65 	| 101 	| uInt16LE 	| VDC2 in V/10                                                                                              	|
| 0x66 	| 102 	| uInt16LE 	| IDC2 in A/10                                                                                              	|
| 0x67 	| 103 	| uInt16LE 	| IDC2 in A/10                                                                                              	|
| 0x68 	| 104 	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x69 	| 105 	| uInt8   	| always 0x00 ?                                                                                              	|
| 0x6A 	| 106 	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x6B 	| 107 	| uInt8   	| always 0x00 ?                                                                                              	|
| 0x6C 	| 108 	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x6D 	| 109 	| uInt8   	| always 0x00 ?                                                                                              	|
| 0x6E 	| 110 	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x6F 	| 111 	| uInt8   	| always 0x00 ?                                                                                             	|
| 0x70 	| 112 	| string  	| inverter communication protocol version (ASCII, 8 bytes)                                                   	|
| 0x71 	| 113 	| string  	| inverter communication protocol version                                                                    	|
| 0x72 	| 114 	| string  	| inverter communication protocol version                                                                    	|
| 0x73 	| 115 	| string  	| inverter communication protocol version                                                                    	|
| 0x74 	| 116 	| string  	| inverter communication protocol version                                                                    	|
| 0x75 	| 117 	| string  	| inverter communication protocol version                                                                    	|
| 0x76 	| 118 	| string  	| inverter communication protocol version                                                                   	|
| 0x77 	| 119 	| string  	| inverter communication protocol version                                                                    	|
| 0x78 	| 120 	| string  	| inverter control board firmware version (ASCII, 8 bytes)                                                   	|
| 0x79 	| 121 	| string  	| inverter control board firmware version                                                                    	|
| 0x7A 	| 122 	| string  	| inverter control board firmware version                                                                    	|
| 0x7B 	| 123 	| string  	| inverter control board firmware version                                                                    	|
| 0x7C 	| 124 	| string  	| inverter control board firmware version                                                                    	|
| 0x7D 	| 125 	| string  	| inverter control board firmware version                                                                    	|
| 0x7E 	| 126 	| string  	| inverter control board firmware version                                                                    	|
| 0x7F 	| 127 	| string  	| inverter control board firmware version                                                                    	|
| 0x80 	| 128 	| string  	| inverter communication board firmware version (ASCII, 8 bytes)                                             	|
| 0x81 	| 129 	| string  	| inverter communication board firmware version                                                              	|
| 0x82 	| 130 	| string  	| inverter communication board firmware version                                                              	|
| 0x83 	| 131 	| string  	| inverter communication board firmware version                                                              	|
| 0x84 	| 132 	| string  	| inverter communication board firmware version                                                              	|
| 0x85 	| 133 	| string  	| inverter communication board firmware version                                                             	|
| 0x86 	| 134 	| string  	| inverter communication board firmware version                                                             	|
| 0x87 	| 134 	| string  	| inverter communication board firmware version                                                             	|
| 0x88 	| 134 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                                                 	|
| 0x89 	| 134 	| uInt16   	| always 0x00 ?                                                                                             	|
| 0x8A 	| 138 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                                                 	|
| 0x8B 	| 139 	| uInt16   	| always 0x00 ?                                                                                             	|
| 0x8C 	| 140 	| uInt16   	| rated power in W/10 (big endian! 0x1770 = 6000 = 600 W)                                                    	|
| 0x8D 	| 141 	| uInt16  	| rated power in W/10                                                                                        	|
| 0x8E 	| 142 	| uInt16   	| always 0x02 ? (0x0201 = 513)                                                                               	|
| 0x8F 	| 143 	| uInt16   	| always 0x01 ?                                                                                             	|
| 0x90 	| 144 	| uInt16   	| always 0x00 ? (device type 4 ?)                                                                            	|
| 0x91 	| 145 	| uInt16   	| always 0x04 ?                                                                                             	|
| 0x92 	| 146 	| uInt16   	| always 0x00 ? (0x0001 = 1)                                                                                	|
| 0x93 	| 147 	| uInt16   	| always 0x01 ?                                                                                             	|
| 0x94 	| 148 	| uInt16   	| always 0x00 ? (0x0001 = 1)                                                                                 	|
| 0x95 	| 149 	| uInt16   	| always 0x01 ?                                                                                             	|
| 0x96 	| 150 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                               	                  |
| 0x97 	| 151 	| uInt16   	| always 0x00 ?                                                                                             	|
| 0x98 	| 152 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                                                 	|
| 0x99 	| 153 	| uInt16   	| always 0x00 ?                                                                                              	|
| 0x9A 	| 154 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                                                 	|
| 0x9B 	| 155 	| uInt16   	| always 0x00 ?                                                                                              	|
| 0x9C 	| 156 	| uInt16   	| always 0x02 ? (0x020c = 524)                                                                               	|
| 0x9D 	| 157 	| uInt16   	| always 0x0c ?                                                                                             	|
| 0x9E 	| 158 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                                                	|
| 0x9F 	| 159 	| uInt16   	| always 0x00 ?                                                                                             	|
| 0xA0 	| 160 	| uInt16   	| always 0x02 ? (0x0213 = 531)                                                                               	|
| 0xA1 	| 161 	| uInt16   	| always 0x0c ?                                                                                             	|
| 0xA2 	| 162 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                               	                  |
| 0xA3 	| 163 	| uInt16   	| always 0x00 ?                                                                                             	|
| 0xA4 	| 164 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                                                 	|
| 0xA5 	| 165 	| uInt16   	| always 0x00 ?                                                                                              	|
| 0xA6 	| 166 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                               	                  |
| 0xA7 	| 167 	| uInt16   	| always 0x00 ?                                                                                             	|
| 0xA8 	| 168 	| uInt16   	| always 0x00 ? (0x0000 = 0)                                                                                 	|
| 0xA9 	| 169 	| uInt16   	| always 0x00 ?                                                                                              	|
| 0xAA 	| 170 	| string  	| micro inverter port 1 (16 bytes, ASCII, padded with 0x20 = <space>)                                        	|
| 0xAB 	| 171 	| string  	| micro inverter port 1                                                                                     	|
| 0xAC 	| 172 	| string  	| micro inverter port 1                                                                                      	|
| 0xAD 	| 173 	| string  	| micro inverter port 1                                                                                      	|
| 0xAE 	| 174 	| string  	| micro inverter port 1                                                                                      	|
| 0xAF 	| 175 	| string  	| micro inverter port 1                                                                                     	|
| 0xB0 	| 176 	| string  	| micro inverter port 1                                                                                     	|
| 0xB1 	| 177 	| string  	| micro inverter port 1                                                                                     	|
| 0xB2 	| 178 	| string  	| micro inverter port 1                                                                                     	|
| 0xB3 	| 179 	| string  	| micro inverter port 1                                                                                     	|
| 0xB4 	| 180 	| string  	| micro inverter port 1                                                                                     	|
| 0xB5 	| 181 	| string  	| micro inverter port 1                                                                                     	|
| 0xB6 	| 182 	| string  	| micro inverter port 1                                                                                     	|
| 0xB7 	| 183 	| string  	| micro inverter port 1                                                                                     	|
| 0xB8 	| 184 	| string  	| micro inverter port 1                                                                                     	|
| 0xB9 	| 185 	| string  	| micro inverter port 1                                                                                     	|
| 0xBA 	| 186 	| string  	| micro inverter port 2 (16 bytes, ASCII, padded with 0x20 = <space>)                                        	|
| 0xBB 	| 187 	| string  	| micro inverter port 2                                                                                     	|
| 0xBC 	| 188 	| string  	| micro inverter port 2                                                                                      	|
| 0xBD 	| 189 	| string  	| micro inverter port 2                                                                                      	|
| 0xBE 	| 190 	| string  	| micro inverter port 2                                                                                      	|
| 0xBF 	| 191 	| string  	| micro inverter port 2                                                                                     	|
| 0xC0 	| 192 	| string  	| micro inverter port 2                                                                                     	|
| 0xC1 	| 193 	| string  	| micro inverter port 2                                                                                     	|
| 0xC2 	| 194 	| string  	| micro inverter port 2                                                                                     	|
| 0xC3 	| 195 	| string  	| micro inverter port 2                                                                                     	|
| 0xC4 	| 196 	| string  	| micro inverter port 2                                                                                     	|
| 0xC5 	| 197 	| string  	| micro inverter port 2                                                                                     	|
| 0xC6 	| 198 	| string  	| micro inverter port 2                                                                                     	|
| 0xC7 	| 199 	| string  	| micro inverter port 2                                                                                     	|
| 0xC8 	| 200 	| string  	| micro inverter port 2                                                                                     	|
| 0xC9 	| 201 	| string  	| micro inverter port 2                                                                                     	|  
| 0xCA 	| 202 	| string  	| micro inverter port 3 (16 bytes, ASCII, padded with 0x20 = <space>)                                        	|
| 0xCB 	| 203 	| string  	| micro inverter port 3                                                                                     	|
| 0xCC 	| 204 	| string  	| micro inverter port 3                                                                                      	|
| 0xCD 	| 205 	| string  	| micro inverter port 3                                                                                    	|
| 0xCE 	| 206 	| string  	| micro inverter port 3                                                                                      	|
| 0xCF 	| 207 	| string  	| micro inverter port 3                                                                                     	|
| 0xD0 	| 200 	| string  	| micro inverter port 3                                                                                     	|
| 0xD1 	| 209 	| string  	| micro inverter port 3                                                                                     	|
| 0xD2 	| 210 	| string  	| micro inverter port 3                                                                                     	|
| 0xD3 	| 211 	| string  	| micro inverter port 3                                                                                     	|
| 0xD4 	| 212 	| string  	| micro inverter port 3                                                                                     	|
| 0xD5 	| 213 	| string  	| micro inverter port 3                                                                                     	|
| 0xD6 	| 214 	| string  	| micro inverter port 3                                                                                     	|
| 0xD7 	| 215 	| string  	| micro inverter port 3                                                                                     	|
| 0xD8 	| 216 	| string  	| micro inverter port 3                                                                                     	|
| 0xD9 	| 217 	| string  	| micro inverter port 3                                                                                     	| 
| 0xDA 	| 218 	| string  	| micro inverter port 4 (16 bytes, ASCII, padded with 0x20 = <space>)                                        	|
| 0xDB 	| 219 	| string  	| micro inverter port 4                                                                                     	|
| 0xDC 	| 220 	| string  	| micro inverter port 4                                                                                      	|
| 0xDD 	| 221 	| string  	| micro inverter port 4                                                                                      	|
| 0xDE 	| 222 	| string  	| micro inverter port 4                                                                                      	|
| 0xDF 	| 223 	| string  	| micro inverter port 4                                                                                     	|
| 0xE0 	| 224 	| string  	| micro inverter port 4                                                                                     	|
| 0xE1 	| 225 	| string  	| micro inverter port 4                                                                                     	|
| 0xE2 	| 226 	| string  	| micro inverter port 4                                                                                     	|
| 0xE3 	| 227 	| string  	| micro inverter port 4                                                                                     	|
| 0xE4 	| 228 	| string  	| micro inverter port 4                                                                                     	|
| 0xE5 	| 229 	| string  	| micro inverter port 4                                                                                     	|
| 0xE6 	| 230 	| string  	| micro inverter port 4                                                                                     	|
| 0xE7 	| 231 	| string  	| micro inverter port 4                                                                                     	|
| 0xE8 	| 232 	| string  	| micro inverter port 4                                                                                     	|
| 0xE9 	| 233 	| string  	| micro inverter port 4                                                                                     	|
| 0xEA 	| 234 	| uInt16  	| overfrequency and load reduction starting point (in Hz/100)                                                	|
| 0xEB 	| 235 	| uInt16  	| overfrequency and load reduction starting point                                                            	|
| 0xEC 	| 236 	| uInt16  	| overfrequency and load reduction percentage (in %)                                                         	|
| 0xED 	| 237 	| uInt16  	| overfrequency and load reduction percentage                                                                	|
| 0xEE 	| 238 	| uInt16  	| always 0x00 ? (0x0001 = 1)                                                                                	|
| 0xEF 	| 239 	| uInt16  	| always 0x01 ?                                                                                             	|
| 0xF0 	| 240 	| uInt16  	| always 0x00 ? (0x0000 = 0)                                                                                	|
| 0xF1 	| 241 	| uInt16  	| always 0x00 ?                                                                                             	|
| 0xF2 	| 242 	| uInt16  	| always 0x00 ? (0x0000 = 0)                                                                                	|
| 0xF3 	| 243 	| uInt16  	| always 0x00 ?                                                                                             	|
| 0xF4 	| 244 	| uInt16  	| always 0x00 ? (0x0000 = 0)                                                                                	|
| 0xF5 	| 245 	| uInt16  	| always 0x00 ?                                                                                             	|
| 0xF6 	| 246 	| uInt16  	| grid voltage upper limit (in V/10)                                                                        	|
| 0xF7 	| 247 	| uInt16  	| grid voltage upper limit                                                                                  	| 
| 0xF8  | 248 	| uInt16  	| grid voltage lower limit (in V/10)                                                                        	|
| 0xF9 	| 249 	| uInt16  	| grid voltage lower limit                                                                                  	| 
| 0xFA 	| 250 	| uInt16  	| grid frequency upper limit (in Hz/100)                                                                     	|
| 0xFB 	| 251 	| uInt16  	| grid frequency upper limit                                                                                 	| 
| 0xFC 	| 252 	| uInt16  	| grid frequency lower limit (in Hz/100)                                                                     	|
| 0xFD 	| 253 	| uInt16  	| grid frequency lower limit                                                                                 	| 
| 0xFE 	| 254 	| uInt16  	| start-up self-checking time (in seconds)                                                                   	|
| 0xFF 	| 255 	| uInt16  	| start-up self-checking time                                                                                	| 
| 0x100 | 256 	| uInt8   	| year                                                                                                      	| 
| 0x101 | 257 	| uInt8   	| month                                                                                                      	| 
| 0x102 | 258 	| uInt8   	| day                                                                                                       	| 
| 0x103 | 259 	| uInt8   	| hour                                                                                                      	| 
| 0x104 | 260 	| uInt8   	| minutes                                                                                                    	| 
| 0x105 | 261 	| uInt8   	| seconds                                                                                                    	| 
|       |     	|         	|                                                                                                           	|
| ..    | ..   	| tbd     	| tbd                                                                                                       	|  
|       |     	|         	|                                                                                                           	|
| ---- 	| --- 	| -------- 	|                                                                                                           	|
| 0x221	| 545 	| uInt8    	| checksum - add all bytes, except first, last, and checksum itself, then mod 256                           	|
| 0x222	| 546 	| uInt8    	| always 0x15                                                                                                	|
