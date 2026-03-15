# RDS AI Decoder
An AI-powered RDS monitor for fm-dx-webserver that uses machine learning to predict and correct PS and RadioText data even under poor reception conditions.
<img width="1592" height="846" alt="Image" src="https://github.com/user-attachments/assets/3ba0548a-911b-4377-b128-2209bf131448" />

## Version 1.0

- AI-powered PS correction – Missing or corrupted PS characters are predicted and corrected using machine learning (voting, bigram detection, DB cache)
- Confidence-based rendering – Every PS and RT character is colour-coded by reliability, ranging from near-black (uncertain) to near-white (verified)
- RadioText fusion – Current and previous RT text are displayed side by side; AI results and raw reception are intelligently merged
- RDS Follow mode – Administrators can feed the AI output directly into the FM-DX Webserver with a single button press, replacing the native decoder
- Real-time WebSocket connection – Receives raw data and AI results via /data_plugins; automatic reconnection on connection loss
- Group monitor – All received RDS groups (0A–15B) are displayed live and highlighted on reception
- BER indicator – Bit error rate of the last 60 frames shown as a colour-coded progress bar (green / orange / red)
- Statistics panel – Breakdown of PS slots by source (raw, DB, AI votes, bigram, verified) plus AI connection status and group count
- Toast notifications – Visual alerts on successful WebSocket connect and when a plugin update is available (with version comparison)
- Draggable panel – Freely positionable, closable overlay panel with seamless integration into the fm-dx-webserver plugin system

## Installation notes:

1. [Download](https://github.com/Highpoint2000/RDS-AI-Decoder/releases) the last repository as a zip
2. Unpack all files from the plugins folder to ..fm-dx-webserver-main\plugins\ 
3. Stop or close the fm-dx-webserver
4. Start/Restart the fm-dx-webserver with "npm run webserver" on node.js console, check the console informations
5. Activate the sysinfo plugin in the settings
6. Stop or close the fm-dx-webserver
7. Start/Restart the fm-dx-webserver with "npm run webserver" on node.js console, check the console informations 
8. Reload the browser

## How to use:     
                                         
- Click the RDS Decoder button to open the RDS monitor panel 
- As an administrator, you can activate RDS Follow Mode. This will feed the plugin's RDS data directly into the web server

Detailed documentation on how the plugin works can be found [here](https://highpoint.fmdx.org/manuals/RDS-AI-Decoder-Documentation.html)
A demo video can be viewed [here](https://highpoint.fmdx.org/videos/RDS-AI-Decoder-Demo.mp4)

## Notes: 

- All data is cached in the file rdsm_memory.json in the specific plugin folder. Different retention periods apply to the data
- Once activated, Follow Mode remains active even after a restart, as long as the file rdsm_memory.json is not deleted

## Contact

If you have any questions, would like to report problems, or have suggestions for improvement, please feel free to contact me! You can reach me by email at highpoint2000@googlemail.com. I look forward to hearing from you!

<a href="https://www.buymeacoffee.com/Highpoint" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
