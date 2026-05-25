# Spektrum
Spektrum is a audioreactive animation tool which uses the Open Stage Control webserver features to send the animations to other devices.
It analizes the mikrophone input and sends midi data at range [ch4c20 ch4c27] \
Open Stage Version used: 1.30.3


### Guide
To use this project, you need to install TouchDesigner and Open Stage Control. Both are free (TouchDesigner is free for non-commercial use). Also you need a virtual midi port emulator (I recomend loopMIDI). Here you can download them: \
https://derivative.ca/download  \
https://openstagecontrol.ammd.net/download/ \
https://www.tobias-erichsen.de/software/loopmidi.html

Define 2 midi-ports in the midi port emulator software you have chosen. Name them as you want.\

Open Touchdesiner and open the Spektrum file.
Then start OpenStageControl, then select the controller from your files. Type "OSC:[midiport1name],[midiport2name]" in the MIDI-frame. *([midiport1name] is output, [midiport2name] is input for the DAW)*\
Launch the server.\

You also can use your phone, tablet or any other computer with internet access. Just type in the URL shown in OpenStageControl or scan the QR-Code.

### Walktrough
#### Touchdesigner Interface
When opened the Spektrum file via touchdesigner, you should set the clip range to a range that fits your usecase. Select the limit1 operator and change the minimum value:
<img width="2880" height="1778" alt="Screenshot 2026-05-25 225253" src="https://github.com/user-attachments/assets/efbbe0f7-423b-4002-ae4b-3b5510000aba" />
For even more control, you can edit the lag1 operator. Higher lag-values flatten the animation while low values make it more reactive. You can also unlink the operator for even higher reactiveness:
<img width="2879" height="1776" alt="Screenshot 2026-05-25 225339" src="https://github.com/user-attachments/assets/a9a7b3ea-f89e-4c7e-8053-753fc3b76734" />

#### Open Stage Control Interface
The main menu looks like this. With the "switch mode" you can switch between the linear and the 2 circular modes:
<img width="2879" height="1774" alt="Screenshot 2026-05-25 223325" src="https://github.com/user-attachments/assets/acd12769-9497-4042-9477-e8c3c19d83e2" />
<img width="2879" height="1771" alt="Screenshot 2026-05-25 223402" src="https://github.com/user-attachments/assets/940ac754-2980-47ad-8f89-9d50dfc29098" />
<img width="2879" height="1776" alt="Screenshot 2026-05-25 223454" src="https://github.com/user-attachments/assets/aa621d3d-7b85-4454-b758-8bb309e35f38" />

With the "change theme" button you can edit both of the systems colors (Color 1 is the main color and also the window color). Use the rgb-fader to select your favs:
<img width="2879" height="1773" alt="Screenshot 2026-05-25 223507" src="https://github.com/user-attachments/assets/14b4bd68-c8b7-4075-8555-a13956184502" />

In the settings tab you can change the scale of the animation. The scale strongly depends on the audio you'rerecording (It should never reach the upper end):
<img width="2879" height="1769" alt="Screenshot 2026-05-25 223527" src="https://github.com/user-attachments/assets/1094671d-c9dc-48c5-ab57-1f54feda1e0e" />
Also you can enable or disable additional lights for both of the circular modes. Lights uses the bass-eq range, while claps uses the high-eq range. You can change the activation value with the fader beside. Also you can change the color of the lights between theme1, theme 2 and white (#ffffff):
<img width="2879" height="1771" alt="Screenshot 2026-05-25 223639" src="https://github.com/user-attachments/assets/3639245f-7502-4d9c-9717-4b4bb93f24c9" />
<img width="2879" height="1768" alt="Screenshot 2026-05-25 223703" src="https://github.com/user-attachments/assets/98917e81-5e05-4ec7-b288-af4f6843ae26" />
<img width="2879" height="1772" alt="Screenshot 2026-05-25 223717" src="https://github.com/user-attachments/assets/164848b6-6b54-40de-93d8-42145fb0793a" />
