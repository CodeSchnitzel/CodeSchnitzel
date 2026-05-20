# A Brief Overview of Projects In The CodeSchnitzel Lab #

Updated 5/20/2026

[toc]

------

## Active Projects (10 projects with 32 sub-projects)

### <u>AI Lab Automation Suite (aka JARVIS)</u>

(/lab-automation) -- An AI-driven laboratory instrument test orchestration suite.  JARVIS constructs and administers complex test and experimental procedures based on natural language requests.  It considers the capabilities & limitations of lab instrumentation, follows safety guidelines and gathers & analyzes data.  JARVIS combines local AI [WOPR](#WOPR Local AI) with cloud-based AI and leverages my local "Deep Knowledge Stockpile" service.

For its first test to ensure it could communicate with instruments, it self-discovered a real problem with a power supply.  JARVIS brought this to my attention and worked through problem identification.   It turned out to be a faulty switch between test instruments.
- Status:
  | Phase                                            | Current Status                                               |
  | ------------------------------------------------ | ------------------------------------------------------------ |
  | 1. Foundational work with local AI engine        | :heavy_check_mark: Completed                                 |
  | 2. Speech services                               | :heavy_check_mark: Completed                                 |
  | 3. Knowledge building (Deep Knowledge Stockpile) | :heavy_check_mark: Completed (but will grow forever)         |
  | 4. Safety & orchestration                        | :thought_balloon: Planning                                   |
  | 5. Skills building & data analysis               | :thought_balloon: / :construction: Planning (AI upgrades underway) |
  | 6. Advanced procedures                           | :thought_balloon: Planning                                   |

### <u>Atomic Director</u>

(/atomic-director) -- A rubidium atomic clock consisting of both custom & commercial hardware with custom software for managing a stack of high precision disciplined time & frequency standards.
- Status:
  - :heavy_check_mark: Equipment rack built
  - :heavy_check_mark: Controller computer with touchscreen built
    - Photo:  <a href="images/atomic-director-development_1080.JPG" target="_blank">Atomic Director rack unit</a>
  - :heavy_check_mark: Signal distributor rack unit built
  - :construction: Protocol Translator designed, firmware is unit-tested -- awaiting in-circuit testing
  - :construction: Controller software architecture is mapped out -- awaiting Comms hardware to begin implementation
  - :construction: Comms system in final engineering stage; PCB designed, prepping for production
    - 3D Rendering:  <a href="images/KB5EO-Atomic-Director-comms-subsystem-PCB-Render-Rev-A-Front.png" target="_blank">Comms circuit board render (front view)</a>
    - 3D Rendering:  <a href="images/KB5EO-Atomic-Director-comms-subsystem-PCB Render-Rev-A-Back.png" target="_blank">Comms circuit board render (back view)</a>
  - :thought_balloon: Switching & Signals systems in scoping
  - :thought_balloon: Power Control & Monitoring in scoping

### <u>Enhance-Enhance</u>

(/enhance-enhance) -- Local AI-augmented video cleanup and upscaling for old home movies.  First for video digitized from Hi-8 and later to couple with an as-yet undefined (but well underway) project to build a custom 8mm film movie digitizer.  No re-inventing the wheel -- this is leveraging mostly common open source tools and some commercial software.

- Status:
  - :construction: Foundations & data model0
  - :thought_balloon: Cleanup pipeline
  - :thought_balloon: Scene detection
  - :thought_balloon: Thermal supervisor (control CPU and GPU heat)
  - :thought_balloon: Upscaler & encoder
  - :thought_balloon: Metadata tools & static trimming
  - :thought_balloon: Tuning notebook
  - :thought_balloon: Batch & helpers


### <u>Infrastructure Build Out Project</u>

(/infrastructure) -- This is an ever-evolving project to build network services, VM's, LXC containers and physical devices to facilitate all development & lab activities.
- Services in development or in planning:
     - :thought_balloon: Vision services (planned as a part of the Insightful Observer project)
     - :construction: High availability for VM infrastructure
     - :thought_balloon: Conversion of local AI from a VM to a physical machine
     - :construction: NAS upgrades
     - :construction: Main workstation upgrade
- Services deployed:
     - :heavy_check_mark: Upgraded, simplified & hardened firewall
     - :heavy_check_mark: Internal reverse proxy, VPN & certificate authority
     - :heavy_check_mark: Ad & malware blocking (Pi-Hole)
     - :heavy_check_mark: Wide area notifications
     - :heavy_check_mark: Data management stack (SQL Server, Prometheus, InfluxDB)
     - :heavy_check_mark: Data collection & analytics (Mosquitto, Telegraf, Grafana, etc.)
     - :heavy_check_mark: Artificial intelligence core (Ollama, Jarvis, AI tool kits, etc.)
     - :heavy_check_mark: Strategic file sync across devices
     - :heavy_check_mark: SPeech As A Service
     - :heavy_check_mark: Deep Knowledge Stockpile
     - :heavy_check_mark: Internal security layering & monitoring
     - :heavy_check_mark: Internal IoT network
- Status:	Permanent / Ongoing

### <u>Mellanox NIC Active Cooler</u>

(/mellanox-cooler) -- A hardware enhancement for Mellanox MCX4121 NIC cards to prevent them from self destructing due to their pathetically inadequate thermal design.
- Status:	  :construction:  Design complete / Implementation phase

### <u>Serene Sentinel</u> Machine Vision Platform

(/vision/serene-sentinel) -- A platform for small machine vision devices at the computing edge.  This platform directly serves several basic use cases, but also supports the more ambitious [Insightful Observer](#Insightful Observer) project.
- Status:	 :construction: Project charter complete. In architecture scoping & structuring

### <u>STAR TRKR</u>

(/star-trkr) A collection of sub-projects that combine into a hardware and software package for astrophotography.  Named for the command reference silk-screened onto the guidance & navigation control panel in the Apollo Command Module and Lunar Module.

#### *STAR TRKR:  Star Brain*

(/star-trkr/star-brain)  -- The computer and software that control STAR TRKR and interface with various hardware components.
- Status:
  
	| Subsection                 | Status                                                       |
  | -------------------------- | ------------------------------------------------------------ |
  | Main controller computer   | :construction: In prototyping                                |
  | Software development       | :thought_balloon: Scoping                                    |
  | Camera platform            | :heavy_check_mark: Built                                     |
  | Azimuth & elevation stages | :heavy_check_mark: Mechanics built<br />:heavy_check_mark: Elevation is motorized<br />:thought_balloon: Need to build azimuth motor adapter + controller circuits |
  | Polar alignment fixture    | :construction: In mechanical design                          |

#### *STAR TRKR:  Star Finder*

(/star-trkr/star-finder) -- An integration of the [Astro Discovery](#Astro Discovery) project into [Star Brain](#Star Brain) to merge plate solving and eventually polar alignment into the overall platform control.  This will become a software integration with the main controller computer.

#### *STAR TRKR:  Tracker Muscle* (Right Ascension Axis)

(/star-trkr/trkr-muscle) -- A high precision linear actuator to control STAR TRKR's right ascension axis, matching the angular rotation of the Earth to keep camera equipment fixed on a single aimpoint.
- Status:
  - :heavy_check_mark: Kinematics built (carbon fiber linear actuator with a ballscrew drive for micron precision).
  - :heavy_check_mark: Calibration/alignment fixture built.
  - :construction: Motor drive controller prototyped, awaiting round-2 engineering and software integration.
  - :heavy_check_mark: Was used successfully for the April 8, 2024 total solar eclipse using prototype controller.
  	- Photo:  <a href="images/IMG_0218_1080.JPG" target="_blank">STAR TRKR, April 8 2024 Total Eclipse</a>

### <u>Stuff Of Things</u>

(/stuff-of-things) -- Yeah, it had to happen eventually -- the IoT project.  In order for JARVIS to properly interact with the physical world (short of getting a robot body), I needed to give him ears and a voice all around the house and the ability to control lighting, equipment and appliances.  So that leads us into a bunch of control devices and an IoT subnet with all the layers of security that go along with that.

#### *Stuff Of Things:  IoT Network*

(/stuff-of-things/network) -- Dedicated IoT WiFi gateway.  Multi-layer firewall enforcement and strict isolation of devices.

- Status:
  - :heavy_check_mark: Design approved
  - :heavy_check_mark: Installed, penetration tested, telemetry & logging stack working

#### *Stuff Of Things:  Lighting*

(/stuff-of-things/lighting) -- Smart-switch / smart-plug control of lighting & devices via the existing message broker.  Cloud-independent hardware only; no phone-home devices.
- Status:
  - :heavy_check_mark: Several lighting and appliance control devices installed & tested.  First automations built.

#### *Stuff Of Things:  Voice Control & Response*

(/stuff-of-things/voice) -- A fun feature of this project is a bunch of smart microphones that have just enough intelligence to listen for an activation phrase, then stream whatever verbal command that follows to JARVIS.  This gives JARVIS location awareness and the ability to direct verbal responses to the right location as well as understanding the context of commands.  "Lights on" means something different depending on where it's spoken.

No cloud.  No internet.

For now, the idea is to have enough self-designed & built smart microphones around the house to make this work, but it may evolve into phased microphone arrays that can sense direction from a single point.

- Status:
  - :heavy_check_mark: Planning complete
  - :heavy_check_mark: JARVIS AI agent tool for device control implemented
  - :heavy_check_mark: Hardware for the first 3 smart mic prototypes in-hand
  - :construction: Phase 1 smart mic prototype bring-up paused due to other lab work competing for resources

### <u>ThermaLog</u>

A high precision, high accuracy logger that monitors multiple platinum wire temperature sensors as well as ambient environment conditions.  ThermaLog emphasizes oversampling and precisely time-correlated measurements for both real time and offline analysis.
- Status:
  - :heavy_check_mark: Fully prototyped & tested
  - :heavy_check_mark: Prototype is in regular use in the lab and getting periodic firmware improvements
  - :construction: Pre-production validation for a finished package in progress (not public yet)

### <u>VetteDirectional</u>

(/VetteDirectional) -- Implementation of a circuit devised by George to permit usage of LED marker and turn signal bulbs in old GM vehicles.
- Status:	 :construction: Pre-production validation


------


## Completed Projects (7 projects) ## 

### [<u>Astro Discovery / Star Finder</u>](#https://github.com/CodeSchnitzel/astro-discovery)

(/astro-discovery) -- Started as a portable VM for running plate solver software in the field to analyze an astrophotography photos and determine, based on stored star maps, what the point of aim, orientation and field of view are.  The project morphed into a Raspberry Pi Zero 2W appliance that can optionally connect directly to the camera and present a user interface through a WiFi connected phone.  It calculates point-of-aim error magnitude and direction to speed up accurate aiming.

From concept to working device in about 3 hours.

This project will later be incorporated into the [STAR TRKR](#STAR TRKR) project, but it is currently autonomous and presents its UI via a web browser on a cell phone or tablet.

- Status:	 :heavy_check_mark: Complete / awaiting field testing if we ever have clear skies again
    - Photo:  <a href="images/astro-discovery-device_1080.jpg" target="_blank">Astro Discovery device (Raspberry Pi Zero)</a>
    - Screen shot:  <a href="images/astro-discovery-ui.jpeg" target="_blank">Astro Discovery user interface</a>

### <u>Chrono Tester</u>

(/speeding-bullet) -- A quick & dirty project to test an Oehler 35P optical chronograph by simulating the photodiodes with 4N25 optocouplers and a microcontroller.

- Status:	 :heavy_check_mark: Complete

### [<u>Photo Deduplicator</u>](#https://github.com/CodeSchnitzel/Photo-Dedupe)

(/photo-dedupe) -- A GoLang program for identifying duplicates among a large collection of photos, regardless of orientation or resolution, using perceptual fingerprinting.  Includes a facility to allow easy confirmation and resolution.

- Status:	 :heavy_check_mark: Complete.  Processed >200,000 photos in the first run.

### <u>Voice Scribe</u>

(/voice-scribe) -- Uses local AI to transcribe voice recorder files into text and then categorize them.  Transcription implemented very successfully on ~250 voice files.  Encountered GPU thermal issues that were resolved via software by taking fan control over from the GPU's driver.

- Status:	 :heavy_check_mark: Complete

### <u>SPaaS</u> (Speech As A Service)

JARVIS and other machines around my network now share centralized on-premise GPU-based Text-To-Speech and Speech-To-Text.  Heavy lifting happens on my [WOPR](#WOPR Local AI) machine (local AI engine).  Audio pickup and delivery is location-aware, but within my lab, it is pipelined to and from a Windows desktop machine via a compiled service because that's where the best audio hardware is.  Any authorized machine that can call an API or connect to a net socket can use the service.  JARVIS has his own unique voice and other devices around the lab have distinct voices as well.

Also implemented VPN to allow secure and seamless conversational access from anywhere via iPhone, iPad, laptop, etc.  This fits the location-aware scheme; voice works on my phone, my laptops or anywhere I am.

- Status:	​ :heavy_check_mark: Complete

### <u>Visual Parts Database</u>

(/visual-database) -- A web-based interactive lookup tool for finding information about parts on assembly drawings.  In its current form, it is a very rich and capable tool to traverse a large and complex radio schematic (Hallicrafters SX42) for restoration.

It lets me click on a component, see detailed specs, record notes & measurements about the original part as well as its replacement if needed.  It highlights what has been done and what needs to be done and integrates both voice recognition and speech synthesis (via [SPaaS](#SPaas (Speech As A Service))) to make the electronics restoration process exceptionally efficient.

In the future, it will gain even more capabilities for a range of other use cases.

- Status:	 :heavy_check_mark: Complete

### <u>WOPR</u> Local AI

A powerful VM with dedicated GPU hardware (PCIe passthrough from the VM host) running Ollama and local LLM / inference models.  Runs Docker to augment speech and other related services.  WOPR is the machine, JARVIS is the personality and knowledge base.

- Status:	 :heavy_check_mark: Complete (conversion from a VM to physical is underway though)

------

## Queued Projects (24 projects) ## 

### <u>3-Channel Optical Chronograph</u>

(/chrono-3chan) -- A modernized version of an Oehler model 35P chronograph with wireless feature for better data management and analysis.  Will likely use a browser with a phone or tablet as the UI.

- Status:	 :thought_balloon: Scoping

### <u>7-Segment LED Display</u>

(/displays/led7seg-driver) -- A simple, expandable multi-line LED display.  Complements the [RPN Calculator](#RPN Calculator) and [EZ Clock](#EZ Clock) projects.

- Status:	 :construction: Feasibility tested

### <u>Acoustic Laser</u>

(/acoustic-laser) -- OK, not a laser, but a collection of acoustic beamforming experiments.  I'm mostly interested in adaptive sound delivery but also curious about microphone matrix arrays.

- Status:	 :thought_balloon: Scoping

### <u>Acoustic Trilaterator</u>

(/acoustic-trilaterator) -- Microphone array for pinpointing bullet location on a target by signal analysis of the shockwave's acoustic signature and time-difference-of-arrival.

- Status:	 :thought_balloon: Scoping

### <u>Barbara Mandrel</u>

(/mandrel-4humanity) -- A 3D design and engineering project to save humanity and all its dependencies by solving toilet paper frustrations.  :smile:  (NO RELATION whatsoever to Barbara Mandrell, who is a 3D person)

- Status:	 :thought_balloon: Conceptual

### <u>Bobcat 225G Engine Idler</u>

(/bobcat-idler) -- A modern replacement for an automatic idle-down circuit for the engine on Miller Bobcat 225G welder/generators.  This is to replace a part that is now unobtanium.

- Status:	 :thought_balloon: Experimental / awaiting redesign

### <u>Insightful Observer</u>

(/vision/insightful-observer) -- A server-side observation system.  Leveraging the Serene Sentinel platform, camera devices report captures and metadata to an ingest endpoint; the server stores them, classifies them, analyzes content and surfaces significant events through dashboards and alerts. Hosts two server-bound products: *door-cam* (single-cam target classifier) and *field-mesh* (battery-powered mesh group with on-device pre-filtering).

- Status:	 :thought_balloon: Charter restructured around server-side scope; awaiting lab infrastructure maturation and [*Serene Sentinel*](#Serene Sentinel) platform stabilization before product work begins

### <u>EZ Clock</u>

(/easy-clock) -- Inexpensive, hassle-free clocks that can be placed anywhere within range of a WiFi network with NTP access.  Modular for a choice of displays including round TFT's that show traditional clock/watch faces, 7-segment displays, Burroughs Panaplex displays and even speech synthesis.  Benefits from the [7-Segment LED Display](#7-Segment LED Display) project and [Panaplex Plasma Display Driver](#Panaplex Plasma Display Driver) project.

- Status:	 :thought_balloon: Awaiting prioritization (prototyping / POC is done)

### <u>Gauss B Gone</u>

(/degauss-parts) A device that properly degausses small parts according to scientific principles rather than how cheaply can it be made.

- Status:	 :thought_balloon: Awaiting prioritization

### <u>Keithley SCAN2000 Card Clone</u>

(/external-repos/scan2k-clone) -- This is an implementation of a third-party project by "[cozdas](https://github.com/cozdas/CozScan2020)" to replicate a Keithley SCAN2000 20-channel data acquisition scanner but with SSR's instead of mechanical relays.

- Status:	 :thought_balloon: Awaiting prioritization

### <u>Laboratory Clock Generator</u>

(/clock-gen) -- A lab device for producing pulse trains over a wide range of user defined frequencies, based on an Si5354 frequency synthesizer chip.  A central feature is a friendly user interface and extended feature set that are substantially different than other Si5354 projects.

This will have an internal temperature-compensated crystal oscillator (with an auto calibration procedure that will benefit from the "OCXO Calibrator" project), plus the ability to run with an external frequency reference ("[Atomic Director](#Atomic Director)").

- Status:	 :construction: Awaiting version 2 reengineering

### <u>Laboratory DC UPS</u>

(/dc-ups) -- A high efficiency intelligent lithium battery based UPS for powering lab equipment that runs on DC power.

- Status:	 :thought_balloon: Scoping

### <u>Terrain Line-Of-Sight Calculator</u>

(/splat-los) -- A tool for calculating line of sight on the surface of the Earth from any altitude based on radar terrain elevation data collected by Space Shuttle Endeavor, STS-99 on the Shuttle Radar Topography Mission (SRTM) in February 2000.

Useful for estimating terrestrial radio coverage.  Inspired by tools published by Green Bay Professional Packet Radio.

- Status:	 :thought_balloon: Data gathered / awaiting prioritization, considering more modern datasets

### <u>Mains Monitor</u>

(/mains-monitor) -- Lab instrument for characterizing power line frequency drift, voltage consistency and long term accuracy.  Uses a zero-crossing detector to measure against the Atomic Director output reference.

- Status:	 :thought_balloon: Scoping

### <u>OCXO Calibrator</u>

(/ocxo-cal) -- An automated lab instrument for trimming free-running OCXO oscillators to serve as portable short-term time standards for independent data acquisition devices that need to take time-coherent measurements.  Will use Atomic Director as the calibration standard.

- Status:	 :thought_balloon: Scoping

### <u>Panaplex Plasma Display Driver</u>

(/displays/panaplex-driver) -- A modernized circuit to drive early 1970's Burroughs Panaplex displays.  To be used in conjunction with other projects such as [RPN Calculator](#RPN Calculator) and [EZ Clock](#EZ Clock).

- Status:	 :thought_balloon: Data gathering

### <u>PC Cooler Override</u>

(/cooler-override) -- Interposer device to allow a PC motherboard to control PC fans as normal, but to intervene and increase RPM when motherboard controls fail to manage thermal conditions.

- Status:	 :thought_balloon: Requirements gathering

### <u>Quantum Keygen</u>

(/quantum-keygen) -- A high entropy cryptography key generator based on radioactive decay and other sources of true entropy.

- Status:	 :thought_balloon: Feasibility study

### <u>Retro Crypto</u>

(/retry-crypto) -- An anachronistic cryptography device based on a massive array of obsolete Intel 8294A 56-bit DES encryption chips.

- Status:	 :thought_balloon: Hardware acquired / awaiting prioritization

### <u>RPN Calculator</u>

(/rpn-calculator) -- A Reverse Polish Notation calculator that is both imminently practical and amusingly anachronistic.  Utilizes math libraries from CERN and offers extreme modularity of keyboard inputs, display options and API integration.  Combines the most-loved features of my many calculators and omits the things I dislike.

- Status:	 :thought_balloon: Scoping / awaiting prerequisites

### <u>TEC Controller</u>

(/tec-controller) -- Hardware and software to drive thermoelectric (Peltier) devices to control temperature in a test chamber using PID loops.

- Status:	 :thought_balloon: Scoping

### <u>Telephone Ring Generator</u>

(/ring-generator) -- A circuit to ring a classic Western Electric telephone bell from a low voltage lithium battery.  A prerequisite to turn a rotary dial phone into a Bluetooth terminal.

- Status:	 :thought_balloon: Scoping

### <u>YIG Oscillator Driver</u>

(/yig-driver) -- Experimental circuits to learn fine control of Advantek and Hewlett Packard YIG oscillators.

- Status:	 :thought_balloon: Scoping>