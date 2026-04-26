# Hexacopter — The Engineer's Side of an Unfinished Aerial Photography Build

> *I was one of the first hobby DJI Phantom owners. I got beautiful aerial skyline photos. I lost the drone to a fly-away during a demo at Bracketron. The community rebuilt me through a fully-funded Kickstarter. The replacement is a six-rotor DSLR-lift platform with a 3D-printed gimbal — fully assembled but not yet flown, because I lacked confidence in the speed-controller and flight-controller programming. This repository is what I have written down.*

*Hero photo forthcoming: strongest candidates are a finished-build photo of the hexacopter on the bench, a Phantom-era skyline aerial, or a CAD render of the gimbal.*

## What this is

Engineering documentation for a hexacopter aerial-photography platform that I designed, sourced, partially assembled, and then deliberately stopped working on — because the next step was firmware-level speed-controller and flight-controller programming, and I wasn't confident enough to risk a multi-thousand-dollar airframe (much of it crowdfunded) on a maiden flight I wasn't sure of.

The build is currently at my parents' house, intact, ready to be picked up again. This repository captures the engineering work that *did* happen — the BOM, the design choices, the sketchbook entries, the engineering-notebook pages, the 3D-printed gimbal, the CAD — independent of the airframe ever flying.

## The story

### Phantom era — early adopter, beautiful aerials

I was one of the first hobby owners of the **DJI Phantom** when it launched in 2013. Got a string of beautiful aerial skyline photos that — for a brief moment, before consumer drones became ubiquitous — felt like access to a perspective hardly anyone else had.

### The fly-away

During a demonstration to coworkers at **Bracketron**, the Phantom executed a fly-away — flew off in an unintended direction at altitude under conditions I couldn't recover from — and was never seen again. Fly-aways were a known failure mode of early hobby drones; ours was a textbook case (almost certainly a compass-calibration / GPS-handoff event), but the textbook didn't help me get my drone back.

### Crowdfunded rebuild — the hexacopter

I launched a **Kickstarter** to crowdfund a more capable replacement aerial-photography platform. The campaign was fully funded by friends, coworkers, and people who'd seen the Phantom-era photos. With the funds I:

- Sourced a **pre-built hexacopter frame kit** specced for **DSLR camera lift capacity** (six rotors, redundant lift, larger payload than a Phantom-era quad)
- Selected and procured all electronics — flight controller, ESCs, motors, props, telemetry radio, FPV transmitter, receiver, batteries
- Designed and **3D-printed a custom gimbal** for the DSLR payload (one of my first serious 3D-printed mechanism designs)
- Mechanically assembled the airframe + gimbal + electronics
- Wired the power distribution, signal lines, and telemetry

### The decision not to fly

The next step was tuning: program the **speed controllers** (ESCs), configure the **flight controller** firmware (likely an early-era ArduPilot or Naza-class board, depending on the BOM line), set up failsafes, fly small hover tests with reduced gain to bring the PID loops in. I'd done the mechanical and electrical work to a level I trusted. I had not done enough firmware tuning on systems that mattered to feel confident throwing this airframe into the sky.

So I stopped. The hexacopter went into storage at my parents' house and has been waiting since.

The engineering judgment I've made peace with: **stopping was the right call at the time.** Hobby drone fly-aways and crashes from misconfigured firmware are common, and a crowdfunded build deserved more flight-control expertise than I had. The build is still flyable; the firmware learning curve is now much friendlier (modern ArduPilot/Betaflight/PX4 documentation, simulator-first tuning, vastly better community resources). It's a project I can resume rather than restart.

## Why an unfinished build still belongs in the portfolio

**Documentation discipline is independent of execution discipline.** This repository is unusual because the deliverable doesn't fly — but the engineering value isn't in the airframe state, it's in the documented design work. What's documented:

- **Bill of materials** — a complete, sourced, costed component list for a DSLR-lifting hexacopter circa 2013–2015
- **Mechanical design** — frame selection, motor + prop sizing, gimbal CAD, payload geometry
- **3D-printed gimbal** — early CAD-and-print mechanism design, one of my first
- **Electronics architecture** — power distribution, ESC + flight-controller integration, telemetry radio, FPV link
- **Sketchbook + engineering-notebook entries** — design decisions and tradeoff thinking from the time
- **Cross-domain integration** — mechanical, electrical, embedded firmware (incomplete), data comms, payload optics

A senior R&D engineer reading this should see: *here's someone who took on a multi-disciplinary integration project, did the mechanical and electrical work to assembly, recognized when their firmware skill wasn't sufficient for safe execution, and stopped — without pretending they'd finished.* That's a hiring-manager-relevant signal.

## Engineering content (forthcoming)

Material exists in personal archives and at my parents' house; will be added as recovered. The current repo is README + LICENSE only.

| Section | Status |
|---|---|
| Repo description, license | ✓ done |
| Story arc + framing | ✓ this README |
| Phantom-era aerial photos | forthcoming — hero candidate |
| Bill of materials | forthcoming — exists in engineering notebook |
| Mechanical design — frame + motor sizing | forthcoming |
| 3D-printed gimbal CAD + photos | forthcoming |
| Electronics architecture diagram | forthcoming |
| Sketchbook + engineering-notebook scans | forthcoming (parents' house archives) |
| Build photos | forthcoming |
| Firmware-tuning plan (for resumption) | forthcoming |

## Cross-references and the wrfcoin tie-in

Two cross-links worth being explicit about:

- **[wrfcoin](https://www.wrfcoin.com)** — my IoT-to-blockchain weather-data project. A finished hexacopter would make an excellent **mobile sensor platform** for wrfcoin: the current sensor work is fixed-location ground-station based, but a UAV-mounted instrument package could capture vertical atmospheric profiles, micro-climate variation, and remote-area weather data the ground stations can't reach. **Telemetry, payload integration, and data-comms work in this repo would feed directly into a wrfcoin sensor-payload subsystem.**
- **General engineering portfolio** — this is the multi-disciplinary integration project in the personal-craft cluster, alongside [`woodworking`](https://github.com/tonykoop/woodworking) and [`chessboard-table`](https://github.com/tonykoop/chessboard-table). Where those repos document hand-craft, this documents systems-engineering thinking applied to a hobby project.

## Repository structure

```
hexacopter/
├── README.md                  ← you are here
├── LICENSE                    ← CC-BY 4.0
└── (forthcoming)
    ├── images/                ← Phantom skyline photos, build photos, gimbal renders
    ├── CAD/                   ← gimbal + payload-mount geometry
    ├── BOM/                   ← bill of materials, sourcing notes
    ├── electronics/           ← architecture diagram, ESC + FC documentation
    ├── notebook/              ← scanned sketchbook + engineering notebook entries
    └── firmware-plan/         ← tuning + maiden-flight plan (for resumption)
```

## License

Released under [CC-BY 4.0](LICENSE) — original written content, CAD, BOM, photographs, and engineering analysis in this repository are mine, free to reuse and adapt with credit. **Component selections and sourcing decisions documented here are personal-build choices for a hobby project; reproduce at your own risk** (firmware tuning matters, see story above).
