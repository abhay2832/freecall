📞 FreeCall — Simple Peer-to-Peer Video Calling

<div align="center"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=667EEA&center=true&vCenter=true&width=600&lines=Welcome+to+FreeCall;Connect+Anywhere%2C+Anytime;Simple+Browser-Based+Video+Calling" alt="FreeCall Animated Heading" />Connect with people. No complicated setup.

A lightweight browser-based video calling application built with HTML, CSS, JavaScript and PeerJS.

<br><img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
<img src="https://img.shields.io/badge/PeerJS-WebRTC-blue?style=for-the-badge" alt="PeerJS" /><br><br>

🌐 Live Project

https://abhay2832.github.io/freecall/

</div>---

📖 About The Project

FreeCall is a browser-based Peer-to-Peer (P2P) video calling application designed to make online communication simple and accessible.

The project allows two people to connect through a unique Peer ID and communicate using their camera and microphone.

The main idea is simple: open the website, share your Peer ID, enter another person's ID and start a video call.

There is no separate application to install and no account registration system implemented in the current version.

FreeCall uses PeerJS to simplify WebRTC communication between browsers.

🎯 Project Purpose

The purpose of FreeCall is to explore and demonstrate how real-time communication can be implemented using modern web technologies.

The project focuses on:

- Making video calling simple.
- Exploring Peer-to-Peer communication.
- Understanding WebRTC technology.
- Using browser camera and microphone APIs.
- Learning real-time media streaming.
- Creating an interactive and responsive interface.
- Building a functional application using core web technologies.

✨ Features

🆔 1. Automatic Peer ID Generation

When a user opens FreeCall, the application initializes PeerJS and generates a unique Peer ID.

This ID identifies the user for incoming and outgoing calls.

📋 2. Copy Peer ID

Click the displayed Peer ID to copy it to the clipboard.

The application displays a temporary confirmation after copying.

📞 3. Connect Call

Enter another person's Peer ID and click the Connect Call button.

The application requests camera and microphone access before attempting to establish the call.

🎥 4. Live Video Calling

Communicate through live video using the browser camera.

The interface displays both local and remote video streams.

🎙️ 5. Audio Communication

The application captures microphone audio and sends it through the WebRTC media connection.

🔇 6. Mute and Unmute

Control your microphone during an active call.

- Mute disables the outgoing audio track.
- Unmute enables the audio track again.

📹 7. Video Control

Enable or disable the outgoing camera video track during a call.

📴 8. End Call

End an active call whenever required.

The application closes the call, stops local media tracks and clears the video elements.

📱 9. Responsive Interface

The layout includes mobile-specific CSS adjustments for smaller screens.

🎨 10. Modern Visual Design

The interface includes:

- Purple gradient background.
- Translucent white container.
- Rounded buttons and input fields.
- Smooth hover transitions.
- Animated call screen appearance.
- Clean video display.
- Connection status indicators.

---

⚙️ How Does It Work?

FreeCall uses PeerJS and WebRTC to establish real-time communication between two browsers.

Connection Process

       USER 1
          |
          v
    Opens FreeCall
          |
          v
    Peer ID Generated
          |
          v
    Shares Peer ID
          |
          |
          v
       USER 2
          |
          v
    Opens FreeCall
          |
          v
    Enters User 1 ID
          |
          v
    Requests Camera
    and Microphone
          |
          v
    PeerJS Call Setup
          |
          v
    WebRTC Connection
          |
          v
    Audio + Video
          |
          v
     Live Communication

Technical Explanation

1. Peer Initialization

The "initPeer()" function creates a PeerJS instance and initializes the peer connection.

2. Peer ID Generation

The "peer.on('open')" event receives the generated Peer ID and displays it on the screen.

3. Media Access

The application uses:

navigator.mediaDevices.getUserMedia({
    video: true,
    audio: true
});

This requests access to the camera and microphone.

4. Starting a Call

The application uses:

peer.call(peerId, localStream);

This initiates an outgoing call to the specified Peer ID.

5. Handling Incoming Calls

The application listens for incoming calls using:

peer.on('call', (call) => {
    // Handle incoming call
});

6. Receiving Remote Video

The remote media stream is received through:

call.on('stream', (remoteStream) => {
    remoteVideo.srcObject = remoteStream;
});

7. Ending a Call

The "endCall()" function closes the current connection, stops local media tracks and resets the interface.

---

🛠️ Technologies Used

The project uses three core programming languages.

Technology| Usage
HTML5| Application structure
CSS3| Design, layout and animations
JavaScript| Application logic and interactions
PeerJS| Peer connection management
WebRTC| Real-time audio/video communication
STUN| Network discovery assistance
GitHub Pages| Website hosting

Programming Language Count

<details>
<summary>View language details</summary>1. HTML5

Used to create the application structure, buttons, input fields and video elements.

2. CSS3

Used for gradients, layouts, responsive styling, hover effects and transitions.

3. JavaScript

Used for PeerJS initialization, media access, event handling, calling and call controls.

Total: 3 core web programming languages.

PeerJS is a JavaScript library, not a separate programming language.

</details>---

🖥️ User Interface

FreeCall has two main interface sections.

Main Screen

- Peer ID display.
- Peer ID input field.
- Connect Call button.
- Connection status.

Active Call Screen

- Remote video display.
- Local video preview.
- Mute button.
- Video control button.
- End Call button.
- Call status indicator.

---

🚀 How To Use FreeCall

Follow these simple steps.

Step 1 — Open The Website

Visit the FreeCall website in a supported modern browser.

Step 2 — Get Your Peer ID

Wait until your unique Peer ID appears.

Step 3 — Share Your ID

Click your Peer ID to copy it and send it to your friend.

Step 4 — Enter The Other Peer ID

Your friend can enter your Peer ID into the input field.

Step 5 — Connect

Click the Connect Call button.

Step 6 — Allow Permissions

Allow camera and microphone access when your browser asks.

Step 7 — Start Calling

Once the remote video stream arrives, you can communicate.

Step 8 — Control Your Call

Use the available controls:

- Mute
- Unmute
- Video On/Off
- End Call

---

💻 Run The Project Locally

You can run FreeCall on your computer without installing a complex development environment.

Requirements

- A modern web browser.
- Internet connection.
- Git (optional).

Clone Repository

git clone https://github.com/abhay2832/freecall.git

Open Project Folder

cd freecall

Run Using Python

python -m http.server 8000

Open the following address:

http://localhost:8000

You can also open "index.html" using VS Code Live Server.

Note: Camera and microphone access require HTTPS or a browser-recognized secure local origin such as localhost.

---

📂 Project Structure

The current project uses a single-file architecture.

freecall/
│
└── index.html
    │
    ├── HTML Structure
    ├── CSS Styling
    ├── JavaScript Logic
    ├── PeerJS Integration
    ├── Video Elements
    └── Call Controls

All application code is currently contained in "index.html".

---

🔐 Privacy & Permissions

FreeCall requires camera and microphone permissions to provide video calling functionality.

Important details:

- Camera access requires user permission.
- Microphone access requires user permission.
- PeerJS manages signaling and peer connections.
- WebRTC handles real-time media communication.
- Google STUN servers are configured for network discovery.
- The application does not implement account registration.

WebRTC normally encrypts media transport. However, the project has not been independently security-audited and does not provide a complete privacy guarantee.

---

⚠️ Current Limitations

The current version is intentionally lightweight.

- Supports peer-to-peer calling rather than group calling.
- Requires an internet connection.
- Camera and microphone permissions are necessary.
- Network and firewall restrictions can affect connectivity.
- No dedicated TURN server is configured.
- No text chat feature is implemented.
- No user account system is implemented.

---

🔮 Future Improvements

Possible features for future versions:

- [ ] Group video calling.
- [ ] Real-time text chat.
- [ ] Screen sharing.
- [ ] Call duration timer.
- [ ] Incoming call notifications.
- [ ] Camera selection.
- [ ] Microphone selection.
- [ ] Dark mode.
- [ ] Better mobile experience.
- [ ] Improved connection handling.
- [ ] TURN server support.

These are planned improvement ideas, not currently available features.

---

🧠 What I Learned From This Project

Working on FreeCall provides practical experience with:

- HTML, CSS and JavaScript.
- PeerJS integration.
- WebRTC fundamentals.
- Browser media APIs.
- Camera and microphone handling.
- Real-time video streaming.
- JavaScript events and callbacks.
- DOM manipulation.
- Connection lifecycle management.
- Responsive web design.

---

👨‍💻 Developer & Credits

<div align="center"><img src="https://github.com/abhay2832.png" width="110" alt="Abhay GitHub Avatar" />Abhay

Project Owner & Repository Maintainer

Interested in web development, practical applications and exploring modern web technologies.

GitHub Username: "@abhay2832"

</div>Project Information

Detail| Information
Project| FreeCall
Repository Owner| Abhay
Project Type| Web Application
Architecture| Single HTML File
Core Languages| 3
Main Library| PeerJS
Communication| WebRTC
Hosting| GitHub Pages
Development Team| Not publicly specified

---

🤝 Contributions

Suggestions and improvements are welcome.

You can contribute by:

1. Forking the repository.
2. Creating a new branch.
3. Making improvements.
4. Testing your changes.
5. Submitting a Pull Request.

---

📜 License

No license file is currently specified in the repository. Please contact the repository owner for permission before redistributing or reusing the source code.

---

<div align="center">⭐ Support The Project

If you find FreeCall interesting, consider giving the repository a star.

Every bit of support motivates further development!

📞 FreeCall

Simple communication. Direct connection. Better accessibility.

Made with ❤️ by Abhay

</div>
