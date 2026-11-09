<p align="center">
  <img src="assets/fcu_profile_header.svg" width="100%" alt="Nam Anh Tran | Full-stack Software Engineer | Applied AI · Robotics · GIS" />
</p>

<p align="center">
  Full-stack software engineer working across applied AI, robotics, GIS, and web platforms.
</p>

<p align="center">
  <a href="#chasmata">[ CHASMATA ]</a>
  · <a href="#evat">[ EVAT ]</a>
  · <a href="#aurora">[ AURORA ]</a>
  · <a href="#housing">[ HOUSING ML ]</a>
  · <a href="#guide-my-eyes">[ GUIDE MY EYES ]</a>
  · <a href="https://www.linkedin.com/in/thomas-tran-anh">[ LINKEDIN ]</a>
</p>

---

<a id="chasmata"></a>

### Chasmata — Australian Rover Challenge mission control

Chasmata is the software system for Deakin Competitive Robotics Club’s 2027 Australian Rover Challenge rover, where I am Rover Software Engineering Lead. I coordinate architecture and integration across the GUI, Control, and Autonomous teams. I designed and implemented the browser-based mission-control interface and contributed to the ROS interfaces, BaseStation services, arm-control integration, camera pipeline, and mock rover. The operator interface is shaped by my commercial pilot background and inspired by A320 cockpit design philosophy. Its FMA communicates high-level operational state, ECAM presents alerts and procedures, and System Display pages provide subsystem detail.

<ul>
  <li><strong>Mission control:</strong> Driver and Arm Operator dashboards, FMA, ECAM alerts and procedures, and System Display pages</li>
  <li><strong>Control:</strong> gamepad input, mutually exclusive Drive and Arm control, shared Gimbal priority, MoveIt 2 arm Position control, and direct Manual arm control</li>
  <li><strong>ROS integration:</strong> typed telemetry and shared interface contracts for rover state, control, and alerts</li>
  <li><strong>BaseStation:</strong> hosted Angular interface, ROSbridge connections, MoveIt 2, shared ECAM services, and MediaMTX WebRTC/WHEP camera streams</li>
  <li><strong>Development:</strong> C++ mock rover and integration tests for GUI, ROS, arm trajectories, and camera recovery</li>
</ul>

<p align="center"><strong>Driver mission control</strong></p>

<p align="center">
  <img src="assets/chasmata/pilot.png" width="100%" alt="Chasmata Driver dashboard with camera views and rover controls" />
</p>

<br />

<p align="center"><strong>Arm Ops mission control</strong></p>

<p align="center">
  <img src="assets/chasmata/arm_ops.png" width="100%" alt="Chasmata arm operations dashboard" />
</p>

<br />

<p align="center"><strong>ECAM alerts and procedures</strong></p>

<p align="center">
  <img src="assets/chasmata/ecam.png" width="600" alt="Chasmata ECAM mission-control display" />
</p>

<p>
  <a href="https://github.com/deakin-robotics/Chasmata-2027/tree/main/gui">View GUI repository →</a>
</p>

---

<a id="evat"></a>

### EVAT — explainable EV charging recommendations

An explainable EV charging-station recommendation feature for EVAT, where I served as technical lead. I designed the feature architecture and API contracts, coordinated ownership across a seven-member team, implemented the Python FastAPI recommendation service, and led end-to-end integration across the frontend, Node.js backend, persistence layer, and recommendation service.

<ul>
  <li><strong>Leadership:</strong> proposed the feature, secured Product Owner approval, designed the system flow, and coordinated team ownership</li>
  <li><strong>Recommendation:</strong> filters unreachable stations, ranks candidates with a trained preference model, and returns explanations</li>
  <li><strong>Personalization:</strong> combines predicted selection probability with each user’s recent selection history to nudge rankings toward their preferences</li>
  <li><strong>Fallback:</strong> retains fixed-weight scoring when the trained model is unavailable</li>
  <li><strong>Integration:</strong> resolved authorization, schema, routing-data, and recommendation-history issues across services</li>
  <li><strong>Workflow:</strong> local pull-request validation and GitHub Actions build checks for the frontend and backend</li>
</ul>

<br />

<p align="center"><strong>Charger recommendation feature demo</strong></p>

<p align="center">
  <img src="assets/evat/recommendation-demo.gif" width="720" alt="EVAT charger recommendation feature demo" />
</p>

<br />

<p align="center"><strong>Existing EVAT services and recommendation inputs</strong></p>

<p align="center">
  <img src="assets/evat/existing-evat-services.png" width="100%" alt="EVAT existing services and data sources used by the charger recommendation feature" />
</p>

<br />

<p align="center"><strong>New recommendation pipeline, ranking logic, and persistence</strong></p>

<p align="center">
  <img src="assets/evat/new-recommendation-pipeline.png" width="100%" alt="EVAT new recommendation pipeline with ranking, persistence, and station selection" />
</p>

<p>
  <a href="https://github.com/Chameleon-company/EVAT">View repository →</a>
</p>

---

<a id="aurora"></a>

### AURORA — local AI development assistant

A self-hosted Windows PowerShell AI coding assistant that runs gpt-oss:20b locally through Ollama, uses tool-enabled web search through SearXNG, and exposes private remote access through Tailscale Serve.

<ul>
  <li><strong>Model:</strong> gpt-oss:20b via Ollama</li>
  <li><strong>Context:</strong> 40,960 tokens with Flash Attention</li>
  <li><strong>Memory:</strong> q8_0 KV-cache quantization</li>
  <li><strong>Search:</strong> local SearXNG tool integration</li>
  <li><strong>Remote access:</strong> loopback services published through Tailscale Serve</li>
</ul>

<p align="center">
  <img src="assets/aurora/aurora-demo.gif" width="100%" alt="AURORA local AI assistant using web search and returning a grounded answer" />
</p>

<p align="center"><sub>Fun fact: The name "AURORA" was inspired by APOLLO from <em>Alien: Isolation</em> :D</sub></p>

<p>
  <a href="https://github.com/NamAnhTran99/AURORA">View repository →</a>
</p>

---

<a id="housing"></a>

### Melbourne Housing Price Predictor — deployed regression model

An end-to-end machine-learning project that estimates residential property prices from structured features and exposes the trained model through a Flask web application.

<ul>
  <li><strong>Dataset:</strong> manually collected and structured 151 property listings from Werribee, Point Cook and Tarneit, using AI-assisted extraction followed by manual verification and cleaning.</li>
  <li><strong>Models:</strong> Linear Regression, Random Forest, and Gradient Boosting comparison</li>
  <li><strong>Result:</strong> Random Forest achieved a held-out R² of 0.7266 with approximately $96.6k MAE</li>
  <li><strong>Deployment:</strong> exported scikit-learn pipeline served through a Flask prediction form</li>
</ul>

<p align="center">
  <img src="assets/housing/app-form.png" width="49%" alt="Melbourne Housing Price Predictor input form" />
  <img src="assets/housing/app-prediction.png" width="49%" alt="Melbourne Housing Price Predictor estimated price result" />
</p>

<p>
  <a href="https://github.com/NamAnhTran99/melbourne-housing-price-predictor">View repository →</a>
</p>

---

<a id="guide-my-eyes"></a>

### Guide My Eyes — bachelor thesis in audio-based vision assistance

An Android accessibility application that combines ARCore depth sensing and on-device object detection to help visually impaired users perceive nearby obstacles through sound.

<ul>
  <li><strong>Depth:</strong> ARCore Depth API for estimating obstacle distance and identifying the nearest path hazard</li>
  <li><strong>Vision:</strong> TensorFlow Lite MobileNet-SSD for on-device object detection</li>
  <li><strong>Audio:</strong> directional sound for obstacle position, pitch variation for distance, and Text-to-Speech for object labels</li>
  <li><strong>Evaluation:</strong> tested on a real Android device across corridor and street scenarios, including latency and battery measurements</li>
</ul>

<p align="center">
  <img src="assets/DemoGuideMyEyes.gif" width="420" alt="Guide My Eyes AR depth prototype demo" />
</p>

<p>
  <a href="https://github.com/NamAnhTran99/GuideMyEyes">View repository →</a>
  </br>
  <a href="docs/DATN-Guide-My-Eyes.pdf">Read thesis (Vietnamese) →</a>
</p>
