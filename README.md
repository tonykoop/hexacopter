# Hexacopter — Systems Integration for a Deliberately Grounded Aerial Platform

> *I was one of the first hobby DJI Phantom owners. I got beautiful aerial skyline photos — 10 of which were later juried into the permanent collection of the University of Minnesota Ambulatory Care Center through Art Force. I lost the Phantom to a fly-away during a demo at Bracketron. The community rebuilt me through a Kickstarter funded at 168% of goal by 94 backers. The replacement is a six-rotor DSLR-lift platform with a 3D-printed gimbal that I intentionally kept grounded until the flight-control stack could be validated. This repository is the engineering record of that build — and a record of an outstanding promise to top-tier backers whose aerial photo shoots are still owed.*

*Hero photo forthcoming: strongest candidates are a finished-build photo of the hexacopter on the bench, a Phantom-era skyline aerial, or a CAD render of the gimbal.*

## What this is

Engineering documentation for a hexacopter aerial-photography platform that I designed, sourced, partially assembled, and then deliberately paused before flight testing. The next step was firmware-level speed-controller and flight-controller setup, and I was not willing to risk a multi-thousand-dollar crowdfunded airframe on a maiden flight that had not cleared a convincing validation path.

The build is currently at my parents' house, intact, ready to be picked up again. This repository captures the engineering work that *did* happen: the BOM, the design choices, the sketchbook entries, the engineering-notebook pages, the 3D-printed gimbal, the CAD, independent of the airframe ever flying.

## The story

### Phantom era — early adopter, beautiful aerials

I was one of the first hobby owners of the **DJI Phantom** when it launched in 2013. I got a string of beautiful aerial skyline photos that, for a brief moment before consumer drones became ubiquitous, felt like access to a perspective hardly anyone else had.

### Aerial work juried into a healthcare-facility installation

In September 2015, **Art Force** — the curatorial program that places original art into University of Minnesota healthcare facilities — juried **21 of my photographs into the permanent collection at the U of M Ambulatory Care Center**, including 10 aerial images. The selection was a paid licensing arrangement ($30 per use × 21 images), and the photographs have been printed and installed in the clinic since.

The aerial pieces in that collection are part of the same body of work the Kickstarter backers funded a more capable drone to extend.

### The fly-away

During a demonstration to coworkers at **Bracketron**, the Phantom executed a fly-away and was never seen again. Fly-aways were a known failure mode of early hobby drones; mine was almost certainly a compass-calibration or GPS-handoff event, but the diagnosis did not change the outcome. The drone and the GoPro mounted to it were gone. Coworkers, my brother, and I spent something like 20–30 collective hours ground-searching the area and never recovered it.

### Crowdfunded rebuild — the hexacopter

In March 2014 I launched a **Kickstarter** to crowdfund a more capable replacement aerial-photography platform. The campaign ran March 3 – April 1, 2014 and raised **$5,065 from 94 backers** — **168% of the $3,000 goal** — over 29 days. Backers were a mix of friends, coworkers, and strangers who had seen the Phantom-era aerial photos.

With the funds I:

- sourced a pre-built hexacopter frame kit specced for **DSLR camera lift capacity**
- selected and procured the electronics: flight controller, ESCs, motors, props, telemetry radio, FPV transmitter, receiver, and batteries
- designed and **3D-printed a custom gimbal** for the DSLR payload
- mechanically assembled the airframe, gimbal, and electronics
- wired the power distribution, signal lines, and telemetry

**Rewards delivered:** signed aerial prints (8″×10″, 11″×14″, 12″×18″), canvas wraps, and the bill-of-materials / build-log document.

**Reward still outstanding:** the top-tier backer reward was an aerial photo or video shoot at a time and place of the backer's choosing, anywhere within 250 miles of Minneapolis. Because the hexacopter never had its maiden flight, the top-tier backers have not received their shoots. This is an open commitment, and finishing the firmware-validation work captured later in this repository is the path back to fulfilling it. The build is paused, not closed.

### The decision to keep it grounded

The next step in 2014 was tuning: program the **speed controllers** (ESCs), configure the **flight controller** firmware, set up failsafes, and then fly increasingly careful test hops. I trusted the mechanical and electrical work. I did not yet trust the validation path strongly enough to put a crowdfunded aircraft in the air.

So I kept it grounded. The hexacopter went into storage at my parents' house and has been waiting since.

The engineering judgment I have made peace with is simple: **keeping it grounded was the right call at the time.** Hobby drone crashes from misconfigured firmware are common, and this build deserved a stronger validation chain than I had in hand. The good news is that the project is resumable rather than lost; the documentation ecosystem around platforms like ArduPilot, PX4, simulators, and safer bench-testing workflows is much better now than it was when I first built it.

## Why an unfinished build with an outstanding obligation still belongs in the portfolio

The value here is not "I launched it." The value is in three things together:

**1. The documented systems work that did happen.**
- **Bill of materials** — a complete, sourced, costed component list for a DSLR-lifting hexacopter
- **Mechanical design** — frame selection, motor and prop choices, gimbal CAD, payload geometry
- **3D-printed gimbal** — early mechanism design work
- **Electronics architecture** — power distribution, ESC and flight-controller integration, telemetry radio, FPV link
- **Sketchbook and engineering-notebook entries** — design decisions and tradeoff thinking from the time, including first-principles geometric analysis of motor-to-prop clearance across quad/hex/octocopter configurations (June 2013)
- **Cross-domain integration** — mechanical, electrical, embedded firmware, data comms, and payload optics

**2. The decision to stop before flying.**
A maiden flight on an unvalidated stack carrying a crowdfunded airframe was a bad risk. The same judgment that says "do not fly this yet" is the judgment a UAV company wants in someone touching their hardware. Hobby drone crashes are common; this one didn't crash because I chose not to put it in the air.

**3. The open promise.**
There are top-tier backers who paid for aerial photo shoots in 2014 and have not received them. That promise still exists. It is one of the reasons this build is paused, not abandoned, and one of the reasons the firmware-validation plan in this repo matters — completing those shoots is what closing the loop on this project looks like.

A senior R&D engineer reading this should see: *here is someone who took on a multi-disciplinary integration project, carried the mechanical and electrical work to assembly, recognized when the validation gate for safe execution had not been met, kept the platform grounded rather than bluffing past that limit, and is on record about the unfinished obligation rather than pretending the project is closed.* That is the signal this repo is meant to carry.

## Engineering content (forthcoming)

Material exists in personal archives and at my parents' house; it will be added as recovered. The current repo is README + LICENSE only.

| Section | Status |
|---|---|
| Repo description, license | ✓ done |
| Story arc + framing | ✓ this README |
| Phantom-era aerial photos | forthcoming — hero candidate |
| Selected Art Force / U of M Ambulatory Care Center pieces | forthcoming — selection of the 10 aerial images installed |
| Bill of materials | forthcoming — exists in engineering notebook |
| Mechanical design — frame + motor sizing | forthcoming |
| 3D-printed gimbal CAD + photos | forthcoming |
| Electronics architecture diagram | forthcoming |
| Sketchbook + engineering-notebook scans | forthcoming (parents' house archives) — June 2013 quad/hex/octocopter clearance derivations are top priority |
| Build photos | forthcoming |
| Firmware-tuning plan (for resumption) | forthcoming — ArduPilot / PX4 evaluation, bench-testing sequence, tethered-hover gate, maiden-flight gate |
| Outstanding-backer shoot list (private) | forthcoming — internal tracking, not for public posting |

## Cross-references

- **Art Force / U of M Ambulatory Care Center placement** — Aerial photographs selected for the permanent clinic installation are the body of work this hexacopter was built to extend. Documented in personal archives; selection licensed September 2015.
- **[wrfcoin](https://www.wrfcoin.com)** — a finished hexacopter would make an excellent **mobile sensor platform** for wrfcoin: the current sensor work is fixed-location ground-station based, but a UAV-mounted instrument package could capture vertical atmospheric profiles, micro-climate variation, and remote-area weather data the ground stations cannot reach.
- **General engineering portfolio** — this is the multi-disciplinary integration project in the personal-craft cluster, alongside [`woodworking`](https://github.com/tonykoop/woodworking) and [`chessboard-table`](https://github.com/tonykoop/chessboard-table). Where those repos document hand-craft, this one documents systems-engineering thinking applied to a hobby project.

## Repository structure

```text
hexacopter/
├── README.md                  ← you are here
├── LICENSE                    ← CC-BY 4.0
└── (forthcoming)
    ├── images/                ← Phantom skyline photos, build photos, gimbal renders
    ├── art-force/             ← selection of the 10 aerial images installed at U of M
    ├── CAD/                   ← gimbal + payload-mount geometry
    ├── BOM/                   ← bill of materials, sourcing notes
    ├── electronics/           ← architecture diagram, ESC + FC documentation
    ├── notebook/              ← scanned sketchbook + engineering notebook entries
    └── firmware-plan/         ← tuning + maiden-flight plan (for resumption)
```

## License

Released under [CC-BY 4.0](LICENSE) — original written content, CAD, BOM, photographs, and engineering analysis in this repository are mine, free to reuse and adapt with credit. **Component selections and sourcing decisions documented here are personal-build choices for a hobby project; reproduce at your own risk.** The aerial photographs licensed to Art Force for the U of M Ambulatory Care Center installation are covered separately by that licensing arrangement and are not part of this CC-BY release.
