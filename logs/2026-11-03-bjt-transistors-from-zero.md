# Day 1 — BJT Transistors from Zero
*2026-11-03 · Microelectronics*

I decided to start the transistor from zero here, as a foundation of everything. 

## What a transistor is
A transistor is an electronic component that, in the modern world, we mostly visualize as an electronic switch (it can also amplify). The BJT has two types: **NPN** and **PNP**. The N and P refer to the type of semiconductor:
- **N-type** — doped to have extra free electrons (e.g. with phosphorus).
- **P-type** — doped (e.g. with boron) so it's short an electron, leaving a "hole."

A single **PN** junction is basically a **diode**: current passes mainly from anode (P) to cathode (N), and only when the anode is at a higher voltage than the cathode (by about 0.7 V for silicon).

## Forward vs reverse bias
- **Forward bias** — higher voltage on the anode than the cathode → current flows.
- **Reverse bias** — higher voltage on the cathode than the anode → almost no current.

A normal diode blocks reverse current, but a **Zener diode** is engineered to conduct in reverse once you pass its breakdown voltage.

## Terminals and regions
The transistor has three terminals: **base, emitter, collector**. Any of them can be the common (grounded) reference, but the most common setup is the **common-emitter**.

Three regions of operation:
- **Cutoff** — transistor is off, no current. Both junctions are not forward biased; with 0 input there's no voltage drop across Rc and Rb.
- **Active** — base-emitter forward biased, base-collector reverse biased. This is the **amplifier** region: a small change in Vbe produces a large change in collector current and drops Vc.
- **Saturation** — both junctions forward biased, transistor fully "on."

**Bias** = setting the default (DC) operating current/voltage — the Q-point.

## Gain — β vs α 
Gain exists only in the active region. There are two different ratios, and I mixed them up at first:

- **β (beta) = Ic / Ib ≈ 100** — the collector current is ~100× the base current.
- **α (alpha) = Ic / Ie ≈ 0.99** — ~99% of the carriers injected from the emitter make it to the collector.

So for every ~100 carriers coming from the emitter, about **99 reach the collector (that's α ≈ 0.99)** and only **~1 recombines in the base** — and that 1 is the base current. That gives Ic/Ib ≈ 99–100 = **β**. The strong collector field (from VCC on the collector) is what sweeps those carriers across.


## Transconductance 
**gm = Ic / Vt**, where **Vt** is the **thermal voltage ≈ 26 mV** at room temperature (a constant — *not* Vbe).

gm is really the *slope* ∂Ic/∂Vbe of the exponential Ic = Is·e^(Vbe/Vt); differentiating it gives Ic/Vt.

## Core equations
- Ic = β·Ib
- Ie = Ib + Ic
- Vbe = Vt·ln(Ic/Is)   *(the exponential/ln relationship — still getting fluent with this)*

## Typical DC setup (fixed bias)
A resistor Rb to the base, a resistor Rc to the collector. Apply KVL:
- Base loop: **Vin − Ib·Rb = Vbe**
- Collector loop: **Vcc − Ic·Rc = Vce**

## Where I'm headed next
The prof is already on **input/output impedance** and the three configurations (**common-emitter / base / collector**). I want to catch up. Still shaky on:
- drawing the small-signal model,
- solving circuits with it,
- setting up the KCL/KVL on those.
