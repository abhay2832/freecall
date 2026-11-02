📞 FreeCall — One Page Peer-to-Peer Video Calling

<div align="center"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=25&pause=1000&color=667EEA&center=true&vCenter=true&width=650&lines=Welcome+to+FreeCall+%F0%9F%91%8B;Connect+with+Anyone%2C+Anywhere;Simple+%E2%80%A2+Fast+%E2%80%A2+Browser+Based;No+App+Installation+Required!" alt="Typing SVG" />🌐 Simple. Fast. Free. Connected.

A lightweight browser-based Peer-to-Peer video calling application that allows two people to connect directly using a unique Peer ID.

"🚀 Live Demo" (https://abhay2832.github.io/freecall/) • "📂 Source Code" (https://github.com/abhay2832/freecall)

<br>"HTML5" (https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
"CSS3" (https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
"JavaScript" (https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
"PeerJS" (https://img.shields.io/badge/PeerJS-WebRTC-blue?style=for-the-badge)
"GitHub Pages" (https://img.shields.io/badge/Hosted-GitHub%20Pages-222222?style=for-the-badge&logo=github)

"Status" (https://img.shields.io/badge/Project-Active-brightgreen?style=flat-square)
"Platform" (https://img.shields.io/badge/Platform-Web%20Browser-orange?style=flat-square)
"License" (https://img.shields.io/badge/License-Not%20Specified-lightgrey?style=flat-square)

</div>---

📌 Table of Contents

- "About The Project" (#-about-the-project)
- "Why I Built FreeCall" (#-why-i-built-freecall)
- "Project Information" (#-project-information)
- "Key Features" (#-key-features)
- "How FreeCall Works" (#-how-freecall-works)
- "Technology Stack" (#-technology-stack)
- "Project Architecture" (#-project-architecture)
- "How To Use FreeCall" (#-how-to-use-freecall)
- "Run Locally" (#-run-locally)
- "Browser Permissions" (#-browser-permissions)
- "Privacy and Security" (#-privacy-and-security)
- "Future Improvements" (#-future-improvements)
- "Challenges and Learning" (#-challenges-and-learning)
- "Developer" (#-developer)
- "Contributing" (#-contributing)
- "License" (#-license)

---

🚀 About The Project

FreeCall is a simple, lightweight and browser-based Peer-to-Peer (P2P) video calling application.

The main idea behind FreeCall is to make online communication easier by allowing people to connect with each other directly through a unique Peer ID.

Unlike traditional video calling platforms that require users to create accounts, install applications or complete lengthy registration processes, FreeCall focuses on simplicity.

Users simply:

1. Open the FreeCall website.
2. Get their automatically generated Peer ID.
3. Share their Peer ID with another person.
4. Enter the other person's Peer ID.
5. Click the Connect Call button.
6. Start communicating through a video and audio connection.

The application uses PeerJS and WebRTC technology to establish real-time communication between browsers.

No separate desktop or mobile application installation is required.

<div align="center">💜 Connect Without Complications

Your browser is your communication platform.

</div>---

💡 Why I Built FreeCall

The internet has made communication easier, but many communication platforms still require account creation, application installation and unnecessary setup.

I wanted to explore a different approach.

The idea was to build a small web application where users could start a video call simply by sharing an ID.

The main objectives were:

- Make video calling simple and accessible.
- Understand Peer-to-Peer communication.
- Explore WebRTC technology.
- Learn how browsers handle camera and microphone streams.
- Build an interactive interface using basic web technologies.
- Create a project that works directly inside a browser.
- Understand real-time connection handling and media controls.

FreeCall is also a practical learning project demonstrating how modern browser technologies can be used to build real-time communication applications.

---

✨ Key Features

1. 🆔 Automatic Peer ID Generation

Every user receives a unique Peer ID when opening the application.

This ID is used to identify the user and establish a connection with another peer.

There is no need to manually create an account or username.

2. 📋 One-Click Peer ID Copy

Users can click their generated Peer ID to copy it to the clipboard.

They can then share it through messaging applications or any other communication platform.

3. 📞 Direct Calling System

Enter another user's Peer ID and click the Connect Call button.

FreeCall attempts to establish a real-time connection with the selected peer.

4. 🎥 Live Video Calling

The application supports live video communication through the browser's camera.

Users can see the remote participant once the connection is established.

5. 🎙️ Real-Time Audio Communication

FreeCall captures microphone audio and sends the media stream through the peer connection.

This enables two-way voice communication.

6. 🔇 Mute and Unmute

Users can control their microphone during an active call.

- Mute: Temporarily disables outgoing microphone audio.
- Unmute: Enables the microphone again.

7. 📹 Video On/Off Control

Users can enable or disable their outgoing camera video track during a call.

This gives users more control over their video experience.

8. 📴 End Call

Users can end the current call whenever they want.

The application closes the active connection, stops local media tracks and returns to the main screen.

9. 🎨 Modern User Interface

The interface includes:

- Gradient background.
- Glass-like translucent container.
- Rounded buttons and input fields.
- Hover animations.
- Smooth screen transitions.
- Responsive layout.
- Real-time connection status.

10. 📱 Responsive Design

The layout includes responsive CSS adjustments for smaller screens, making it suitable for mobile and desktop browsers.

---

⚙️ How FreeCall Works

FreeCall uses PeerJS to simplify browser-based WebRTC connections.

Here is the basic working process:

flowchart TD
    A["Open FreeCall Website"] --> B["Initialize PeerJS"]
    B --> C["Generate Unique Peer ID"]
    C --> D["Share Peer ID"]
    D --> E["Other User Enters Peer ID"]
    E --> F["Request Camera and Microphone"]
    F --> G["Create Peer Connection"]
    G --> H["Exchange Media Streams"]
    H --> I["Live Video and Audio Call"]
    I --> J["Mute / Video Controls"]
    J --> K["End Call"]
    K --> L["Stop Media Tracks"]

🔍 Technical Working

Step 1 — Peer Initialization

When the website loads, the "initPeer()" function initializes a new PeerJS instance.

PeerJS generates a unique Peer ID.

Step 2 — Peer ID Sharing

The generated ID is displayed on the interface.

Users can click the ID to copy it and share it with another person.

Step 3 — Camera and Microphone Access

When a user initiates or receives a call, the application requests permission through:

"navigator.mediaDevices.getUserMedia()"

The browser asks the user for camera and microphone permission.

Step 4 — Establishing a Connection

The caller uses:

"peer.call(peerId, localStream)"

PeerJS handles the call setup and WebRTC signaling process.

STUN servers are configured to help peers discover possible network connection paths.

Step 5 — Receiving Remote Media

The application listens for the incoming media stream through:

"call.on('stream', callback)"

Once the remote stream is received, it is displayed inside the remote video element.

Step 6 — Call Management

The application provides functions to manage the active call:

- "handleCall()" — Handles the call and incoming stream.
- "toggleMute()" — Controls microphone audio.
- "toggleVideo()" — Controls camera video.
- "endCall()" — Terminates the call and releases local media resources.

---

🛠️ Technology Stack

FreeCall uses three core web development languages and the PeerJS library.

Technology| Purpose
HTML5| Page structure and video elements
CSS3| Styling, gradients, animations and responsive layout
JavaScript| Application logic and call management
PeerJS| Simplifies WebRTC peer connections
WebRTC| Real-time audio and video communication
STUN| Helps discover network connection paths
GitHub Pages| Website hosting and deployment

Programming Languages

Total core web languages: 3

1. HTML
2. CSS
3. JavaScript

PeerJS is a JavaScript library, not a separate programming language.

---

🏗️ Project Architecture

FreeCall follows a lightweight single-page application architecture.

FreeCall/
│
├── index.html
│   ├── HTML Structure
│   ├── CSS Styling
│   ├── Main Interface
│   ├── Video Elements
│   └── JavaScript Logic
│
└── README.md
    └── Project Documentation

Architecture Explanation

Frontend Layer

Displays the user interface, Peer ID, input fields, call controls and video elements.

Peer Connection Layer

Uses PeerJS to initialize peers, handle signaling and manage calls.

Media Layer

Uses browser media APIs to access camera and microphone streams.

Communication Layer

Uses WebRTC to establish real-time peer-to-peer media communication.

---

📖 How To Use FreeCall

Using FreeCall is simple.

👤 User 1 — Start the Application

1. Open the website.
2. Wait for your Peer ID to generate.
3. Click your Peer ID to copy it.
4. Send that ID to your friend.

👤 User 2 — Connect to User 1

1. Open the same website.
2. Wait for your own Peer ID to generate.
3. Paste User 1's Peer ID into the input field.
4. Click Connect Call.
5. Allow camera and microphone permissions.

🎉 Start Communicating

Once the connection is established:

- See the other participant.
- Talk through your microphone.
- Mute or unmute your microphone.
- Turn your camera on or off.
- End the call whenever needed.

Important: Both users must have access to a compatible browser and an internet connection.

---

💻 Run Locally

Want to explore or modify the source code?

Follow these steps.

Prerequisites

- A computer.
- A modern web browser.
- Git installed.
- Internet connection.

1. Clone the Repository

git clone https://github.com/abhay2832/freecall.git

2. Open the Project Folder

cd freecall

3. Run the Application

Since this project uses a single HTML file, no Node.js backend or package installation is required for the current implementation.

You can open "index.html" through a local development server.

For example, using VS Code Live Server:

1. Open the project folder in VS Code.
2. Install the Live Server extension.
3. Right-click "index.html".
4. Select Open with Live Server.

Alternatively, use Python:

python -m http.server 8000

Then open:

http://localhost:8000

For camera and microphone access, use HTTPS or a browser-recognized secure local development origin such as localhost.

---

🔐 Browser Permissions

FreeCall requires browser permission to access:

- Camera
- Microphone

If permission is denied, the application cannot capture the required media streams.

To fix this:

1. Open the website.
2. Click the browser's site permissions icon.
3. Allow camera access.
4. Allow microphone access.
5. Reload the page if necessary.

---

🛡️ Privacy and Security

FreeCall is designed around browser-based peer communication.

Some important technical details:

- Camera and microphone access require user permission.
- The application does not implement a user account or registration system.
- PeerJS handles connection signaling.
- STUN servers assist with network discovery.
- WebRTC carries the real-time media connection.
- Network conditions and firewall restrictions can affect connectivity.

Privacy Note: The current source code does not include a dedicated privacy policy, authentication system or self-hosted signaling server. Do not treat the application as a fully audited secure communication service. WebRTC normally protects media transport using encryption, but that does not by itself guarantee complete end-to-end privacy across every part of the service.

---

🚀 Future Improvements

FreeCall has a simple foundation that can be expanded with more functionality.

Possible future improvements include:

- [ ] Text chat during calls.
- [ ] Screen sharing.
- [ ] Group video calling.
- [ ] Better connection error handling.
- [ ] Camera selection.
- [ ] Microphone selection.
- [ ] Call duration timer.
- [ ] Incoming call notifications.
- [ ] Improved mobile interface.
- [ ] Dark mode.
- [ ] Custom room IDs.
- [ ] Self-hosted signaling server.
- [ ] Improved accessibility.
- [ ] More robust network connectivity using TURN support.

These are ideas for future development, not features currently implemented.

---

🧠 Challenges and Learning

Building FreeCall provides practical exposure to several important web development concepts.

What This Project Demonstrates

WebRTC Fundamentals

Understanding how real-time communication works inside modern browsers.

Peer-to-Peer Communication

Learning how two users can establish a direct media connection.

JavaScript Event Handling

Working with events such as peer initialization, incoming calls, streams and connection errors.

Browser Media APIs

Accessing and managing microphone and camera streams.

DOM Manipulation

Updating interface elements based on connection state.

CSS Animations

Creating smooth transitions and an interactive interface.

Resource Management

Stopping media tracks and closing connections when calls end.

---

👨‍💻 Developer

<div align="center"><img src="https://github.com/abhay2832.png" width="120" alt="Abhay GitHub Profile Picture" />Abhay

Creator & Project Maintainer

A developer interested in building practical web applications, exploring modern technologies and creating simple solutions to real-world problems.

""GitHub" (https://img.shields.io/badge/GitHub-abhay2832-181717?style=for-the-badge&logo=github)" (https://github.com/abhay2832)

""FreeCall Repository" (https://img.shields.io/badge/Project-FreeCall-blueviolet?style=for-the-badge)" (https://github.com/abhay2832/freecall)

</div>Project Credits

- Project Name: FreeCall
- Project Creator / Repository Owner: Abhay
- Development Approach: Single-page web application
- Repository: abhay2832/freecall
- Deployment: GitHub Pages

The public repository identifies Abhay as its owner. The complete individual or team contribution history has not been established here, so the project is not being incorrectly labelled as exclusively solo-developed.

---

🤝 Contributing

Contributions, suggestions and improvements are welcome.

If you want to contribute:

1. Fork this repository.
2. Create a new branch.
3. Make your changes.
4. Test your implementation.
5. Submit a Pull Request.

git checkout -b feature/new-feature
git add .
git commit -m "Add new feature"
git push origin feature/new-feature

---

📜 License

No license file is currently specified in the repository.

Please contact the repository owner regarding permissions for reuse, modification or redistribution.

---

<div align="center">⭐ Support FreeCall

If you like this project, consider giving it a star on GitHub!

It helps the project gain visibility and encourages further development.

📞 Try It Now

""Open FreeCall" (https://img.shields.io/badge/LAUNCH%20FREECALL-667EEA?style=for-the-badge&logo=googlechrome&logoColor=white)" (https://abhay2832.github.io/freecall/)

""View Source Code" (https://img.shields.io/badge/VIEW%20SOURCE%20CODE-181717?style=for-the-badge&logo=github&logoColor=white)" (https://github.com/abhay2832/freecall)

---

Made with ❤️ by Abhay

Connecting people, one Peer ID at a time.

</div>
