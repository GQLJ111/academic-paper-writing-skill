# Engineering Domain Examples

Use this reference when you need a concrete, field-appropriate framing for an engineering manuscript. Each example shows the same reasoning moves: a controlled central claim, a specific gap, a contribution pattern, method-boundary statements, and safe vs. unsafe claim forms. Adapt the slots to the user's actual study; do not copy numbers or findings.

The shared pattern across all domains:

```text
Central claim: <effect/mechanism> depends on <factor>, <condition>, and <scope> — not a blanket "X always improves Y".
Gap: prior work did <X> under <assumption Y>, leaving <mechanism/condition Z> unresolved.
Contribution: distinguish / decompose / test / quantify, with a stated boundary.
Boundary: "under the tested conditions / simulated setting / specimen set", not universal.
```

---

## 1. Mechanical / Materials / Civil (experiment- and test-led)

Central topic framing:

```text
The fatigue/strength/durability response of <material or component> depends on <load level, microstructure, processing, and environment>, so a single test condition does not characterize service behavior.
```

Avoid: "The proposed treatment improves strength" (no condition, no scope).

Strong gap:

```text
Existing studies characterize <property> mainly under <quasi-static / single-temperature / single-load> conditions, treating <microstructure/defect/interface> as uniform. It remains unclear how <property> evolves under <cyclic loading / elevated temperature / multiaxial stress>.
```

Contribution pattern:

1. Distinguish behavior across processing routes / microstructures / load paths.
2. Isolate one damage or failure mechanism before testing combined loading.
3. Report strength, stiffness, fatigue life, and scatter together, not a single mean.
4. Relate the test-scale result to a service or design boundary.

Method-boundary statements:

```text
To isolate the effect of <microstructure>, specimens were drawn from the same batch and tested under identical surface and environmental conditions. This controls for processing variability but does not capture batch-to-batch or in-service degradation.
```

Safe claim forms: "under the tested load range", "for the specimen geometry used", "the scatter band suggests", "extrapolation beyond the tested cycles is not supported".

Avoid: "the material is stronger" (scope-free), "the result proves field durability", reporting a mean life without scatter or sample size.

---

## 2. Electrical / Control / Automation (method- and system-led)

Central topic framing:

```text
The <controller / estimator / scheduling strategy> improves <stability, tracking, or efficiency> under <modeled dynamics and disturbance>, with performance depending on <model accuracy, delay, and operating point>.
```

Avoid: "The proposed control is better" (no baseline, no condition).

Strong gap:

```text
Prior controllers achieve <objective> under <nominal model / no delay / single operating point>, but it remains unclear whether the guarantee holds under <parameter uncertainty, actuator saturation, communication delay, or disturbance>.
```

Contribution pattern:

1. Formulate the problem (states, inputs, constraints, objective) explicitly.
2. Design the method and state its assumptions and stability/feasibility conditions.
3. Compare against a fair baseline (current practice or accepted method) on matched conditions.
4. Test robustness: perturb parameters, add delay/noise, or harden the scenario.

Method-boundary statements:

```text
Stability is established under <assumption: bounded disturbance, known delay>. The closed-loop result should be read as performance under these assumptions, not as a guarantee under unmodeled dynamics.
```

Safe claim forms: "under the modeled disturbance", "for the tested operating range", "the closed-loop response suggests", "robustness is shown against the perturbations considered".

Avoid: "globally optimal/stable" without proof, claiming hardware performance from simulation only, ablation used as decoration rather than tied to a design choice.

---

## 3. Computer Science / AI / Algorithms (model- and evaluation-led)

Central topic framing:

```text
The proposed <model / algorithm> improves <accuracy, efficiency, or generalization> on <task and data distribution>, with gains depending on <data regime, baseline strength, and evaluation protocol>.
```

Avoid: "Our method achieves state-of-the-art" without matched settings or significance.

Strong gap:

```text
Existing methods perform well on <benchmark / in-distribution setting> but it remains unclear whether the gain comes from <architecture, training data, tuning budget> or transfers under <distribution shift, smaller data, or fairer baselines>.
```

Contribution pattern:

1. Define the problem, notation, and assumptions.
2. Specify the method and what design choice each component serves.
3. Use fair baselines with matched data, tuning budget, and protocol.
4. Report ablations tied to claimed components, plus variance across seeds.

Method-boundary statements:

```text
Baselines were retrained under the same data split and tuning budget to isolate the effect of <component>. Reported gains therefore reflect the component, not extra capacity or longer training.
```

Safe claim forms: "on the evaluated benchmarks", "under matched training budgets", "the ablation indicates", "improvements are within/beyond the seed variance".

Avoid: "best/SOTA" without significance or matched settings, comparing against under-tuned baselines, treating a leaderboard number as a mechanism claim.

---

## 4. Energy / Chemical / Environmental (simulation- and system-led)

Central topic framing:

```text
The <process / system configuration> changes <efficiency, yield, energy use, or emissions> under <feed/load conditions and operating window>, with the effect depending on <operating point, scale, and assumptions>.
```

Avoid: "The new design is more efficient" (no operating window, no baseline).

Strong gap:

```text
Prior studies evaluate <configuration> under <single operating point / idealized feed / steady state>, leaving the <off-design, transient, or scale-up> behavior and the efficiency-cost-emission trade-off unresolved.
```

Contribution pattern:

1. Define the system boundary, feed/load, and reference configuration.
2. Justify operating conditions by design range, standard, or coverage of operating states.
3. Report efficiency, throughput/yield, energy, cost, and emissions together as trade-offs.
4. Test sensitivity to key assumptions and label idealized cases as upper bounds.

Method-boundary statements:

```text
The model assumes <steady state / ideal mixing / fixed feed composition> to isolate the configuration effect. Results represent design-point performance and do not capture transient startup, fouling, or feed variability.
```

Safe claim forms: "at the modeled operating point", "within the simulated operating window", "under the assumed feed", "the sensitivity analysis suggests".

Avoid: "the process is greener/cheaper" without a trade-off boundary, treating a steady-state simulation as field performance, reporting efficiency without the energy or cost it trades against.

---

## 5. Traffic / AV Simulation (worked instantiation)

Central topic framing:

```text
Automated-vehicle car-following behavior affects mixed-traffic efficiency, but the effect depends on behavior type, penetration rate, vehicle arrangement, demand state, and road geometry.
```

Avoid: "Automated vehicles always improve traffic efficiency."

Strong gap:

```text
Existing studies compare AV penetration rates but often treat AVs as a homogeneous class or jump to network-level performance, making it hard to tell whether efficiency changes arise from conservative behavior, cooperative short-headway behavior, disturbance damping, bottleneck discharge, or merging interactions.
```

Contribution pattern:

1. Distinguish behavior types: HDV, conservative AV, cooperative CAV.
2. Decompose longitudinal mechanisms before testing complex road scenarios.
3. Compare pure car-following bottlenecks with merging-transfer scenarios.
4. Report throughput, completion ratio, residual vehicles, travel time, speed/density, and robustness together.
5. Treat pure CAV as an upper bound, not a near-term prediction.

Method-boundary statements:

```text
To isolate driving-behavior effects, all vehicles are modeled as passenger cars and differences among HDV/AV/CAV are represented through car-following parameters. This controls for vehicle length and heavy-vehicle dynamics but does not capture heavy-vehicle share.
```

```text
Lane changing is disabled in this scenario to isolate longitudinal car-following effects; results should be read as car-following effects on bottleneck discharge, not full multi-lane interaction.
```

Safe claim forms: "under the tested SUMO parameters", "in the simulated low-speed bottleneck", "suggests a threshold-like pattern", "should be interpreted as an upper bound".

Avoid: "CAVs are always safer", "higher AV penetration always improves efficiency", "the simulation predicts real-world capacity", "travel-time reduction alone proves higher system efficiency".

---

## How To Use These Examples

1. Pick the closest domain (or combine two if the paper is cross-disciplinary).
2. Reuse the reasoning moves, not the content: controlled central claim, specific gap, 2-4 contributions, explicit method boundaries, scoped claim verbs.
3. If the user's field is not listed, instantiate the shared pattern with the field's own objects, variables, metrics, and boundaries.
4. Never import a number, finding, or citation from these examples into the user's manuscript.
