# Hexacopter — Systems Integration for a Deliberately Grounded Aerial Platform

> *I was one of the first hobby DJI Phantom owners. I got beautiful aerial skyline photos. I lost the drone to a fly-away during a demo at Bracketron. The community rebuilt me through a fully-funded Kickstarter. The replacement is a six-rotor DSLR-lift platform with a 3D-printed gimbal that I intentionally kept grounded until the flight-control stack could be validated. This repository is the engineering record of that build.*

*Hero photo forthcoming: strongest candidates are a finished-build photo of the hexacopter on the bench, a Phantom-era skyline aerial, or a CAD render of the gimbal.*

## What this is

Engineering documentation for a hexacopter aerial-photography platform that I designed, sourced, partially assembled, and then deliberately paused before flight testing. The next step was firmware-level speed-controller and flight-controller setup, and I was not willing to risk a multi-thousand-dollar crowdfunded airframe on a maiden flight that had not cleared a convincing validation path.

The build is currently at my parents' house, intact, ready to be picked up again. This repository captures the engineering work that *did* happen: the BOM, the design choices, the sketchbook entries, the engineering-notebook pages, the 3D-printed gimbal, the CAD, independent of the airframe ever flying.

## The story

### Phantom era — early adopter, beautiful aerials

I was one of the first hobby owners of the **DJI Phantom** when it launched in 2013. I got a string of beautiful aerial skyline photos that, for a brief moment before consumer drones became ubiquitous, felt like access to a perspective hardly anyone else had.

### The fly-away

During a demonstration to coworkers at **Bracketron**, the Phantom executed a fly-away and was never seen again. Fly-aways were a known failure mode of early hobby drones; mine was almost certainly a compass-calibration or GPS-handoff event, but the diagnosis did not change the outcome.

### Crowdfunded rebuild — the hexacopter

I launched a **Kickstarter** to crowdfund a more capable replacement aerial-photography platform. The campaign was fully funded by friends, coworkers, and people who had seen the Phantom-era photos. With the funds I:

- sourced a **pre-built hexacopter frame kit** specced for **DSLR camera lift capacity**
- selected and procured the electronics: flight controller, ESCs, motors, props, telemetry radio, FPV transmitter, receiver, and batteries
- designed and **3D-printed a custom gimbal** for the DSLR payload
- mechanically assembled the airframe, gimbal, and electronics
- wired the power distribution, signal lines, and telemetry

### The decision to keep it grounded

The next step was tuning: program the **speed controllers** (ESCs), configure the **flight controller** firmware, set up failsafes, and then fly increasingly careful test hops. I trusted the mechanical and electrical work. I did not yet trust the validation path strongly enough to put a crowdfunded aircraft in the air.

So I kept it grounded. The hexacopter went into storage at my parents' house and has been waiting since.

The engineering judgment I have made peace with is simple: **keeping it grounded was the right call at the time.** Hobby drone crashes from misconfigured firmware are common, and this build deserved a stronger validation chain than I had in hand. The good news is that the project is resumable rather than lost; the documentation ecosystem around platforms like ArduPilot, PX4, simulators, and safer bench-testing workflows is much better now than it was when I first built it.

## Why an unfinished build still belongs in the portfolio

The value here is not "I launched it." The value is the documented systems work:

- **Bill of materials** — a complete, sourced, costed component list for a DSLR-lifting hexacopter
- **Mechanical design** — frame selection, motor and prop choices, gimbal CAD, payload geometry
- **3D-printed gimbal** — early mechanism design work
- **Electronics architecture** — power distribution, ESC and flight-controller integration, telemetry radio, FPV link
- **Sketchbook and engineering-notebook entries** — design decisions and tradeoff thinking from the time
- **Cross-domain integration** — mechanical, electrical, embedded firmware, data comms, and payload optics

A senior R&D engineer reading this should see: *here is someone who took on a multi-disciplinary integration project, carried the mechanical and electrical work to assembly, recognized when the validation gate for safe execution had not been met, and kept the platform grounded rather than bluffing past that limit.* That is the signal this repo is meant to carry.

## Engineering content (forthcoming)

Material exists in personal archives and at my parents' house; it will be added as recovered. The current repo is README + LICENSE only.

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

- **[wrfcoin](https://www.wrfcoin.com)** — a finished hexacopter would make an excellent **mobile sensor platform** for wrfcoin: the current sensor work is fixed-location ground-station based, but a UAV-mounted instrument package could capture vertical atmospheric profiles, micro-climate variation, and remote-area weather data the ground stations cannot reach.
- **General engineering portfolio** — this is the multi-disciplinary integration project in the personal-craft cluster, alongside [`woodworking`](https://github.com/tonykoop/woodworking) and [`chessboard-table`](https://github.com/tonykoop/chessboard-table). Where those repos document hand-craft, this one documents systems-engineering thinking applied to a hobby project.

## Repository structure

```text
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

Released under [CC-BY 4.0](LICENSE) — original written content, CAD, BOM, photographs, and engineering analysis in this repository are mine, free to reuse and adapt with credit. **Component selections and sourcing decisions documented here are personal-build choices for a hobby project; reproduce at your own risk.**
