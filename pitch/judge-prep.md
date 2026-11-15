# CanopyFlow — judge preparation

Working name. Prepared for a five-minute pitch, weighted toward business application (60%) with AI creativity (40%). All proposed prices, costs, sponsorship terms, timelines and performance goals are planning assumptions. No field results are claimed.

## The answer to remember

We are developing a tractor-towed, camera-guided sprayer for vineyards. It identifies vine foliage, estimates visible canopy density in three fixed spray zones, and times independent valves to match the plant target. We are seeking a founding farm to fund a measured pilot in exchange for two included pilot units and defined support. Success means reduced eligible chemical use with acceptable crop protection, reliable operation and a verified farmer payback.

## The numbers judges will challenge

| Item | Draft assumption | What must validate it |
|---|---:|---|
| Complete trailer selling price | $24,000, tractor excluded | Customer interviews and willingness to pay |
| Cost per complete unit | $14,000 | Supplier quotes, assembly time, installation and warranty |
| Gross profit per paid unit | $10,000 / 41.7% | Actual cost; before overhead and R&D |
| Annual unique acres served | 500 | Row coverage, application speed, pass count and spray windows |
| Eligible annual chemical product cost | $250/acre/year | Farm spray and purchase records; excludes ineligible uses |
| Base chemical-use reduction | 30% | Replicated field measurements and equivalent protection |
| Incremental annual upkeep | $1,500 | Maintenance, software support and service records |
| Base net annual savings | $36,000 | 500 × $250 × 30% − $1,500 |
| Base simple payback | 0.67 years | $24,000 / $36,000; equivalent annualized eight months |
| Low-case simple payback | 5.82 years | 250 acres × $150 × 15% − $1,500 = $4,125 net/year |
| Founding-farm pilot funding | $60,000 | Signed scope, two-unit costs and trial plan |

Savings are annual and seasonal. “Eight months” is an annualized simple-payback equivalent, not a promise about when a farm will receive cash. Payback ignores financing, tax, discounting and resale value. Lower water volume alone is not proof of reduced chemical cost: record product concentration, actual chemical amount and cost per treated acre. Acres are unique annual acres, and annual chemical cost already includes all eligible passes. Do not multiply those values by pass count again.

## Business questions and concise answers

**Who buys this?** The initial buyer is a large vineyard operator or custom applicator. The operations manager owns the budget; an agronomist and equipment manager should approve coverage, compatibility and maintenance. We have not yet established purchase commitments.

**Why would a farm sponsor development?** It receives a defined number of units, input into the requirements, agreed support and measured results from its own operation. This only works if the expected operational benefit and learning value exceed its development risk. Sponsorship is not a proven market signal until a farm signs and funds the scope.

**Why $60,000 when two units would retail for $48,000?** The proposal funds engineering and validation as well as machines. It is not a discounted equipment pre-order. A sponsor must value trial access, development input and support enough to fund the difference. If it only wants equipment, use a normal paid pilot or purchase model instead. Negotiate terms after checking actual build costs.

**What does the farm get for free?** Two included pilot units under the draft sponsorship, delivered after agreed acceptance, plus a defined first-season support package. “Included in sponsorship” is more accurate than “free.” No unlimited units, unlimited lifetime support or automatic exclusivity.

**How do we make money?** Planned sales of complete trailer units, with optional service thereafter. The base model assumes $24,000 price and $14,000 cost, producing $10,000 gross profit before corporate overhead. Do not call gross profit net profit. Ten paid units is a sales scenario, not a forecast or traction.

**What about customer acquisition and service costs?** They are not yet measured. Start with founder-led local farm pilots and referral selling; track site visits, pilot-conversion rate, travel, installation hours and service calls. Budget acquisition and overhead before claiming company profitability. Initial installation and warranty are in the draft unit-cost allowance; avoid counting the same expense twice.

**How big is the market?** USDA NASS reports 883,000 U.S. grape bearing acres for 2025 [S2]. This is crop context, not all serviceable acreage or a customer count. The deck’s 100,000 reachable acres and 500 acres per machine are assumptions: 200 machine equivalents and $4.8 million one-time equipment revenue. A farm can own multiple units. Validate region, row geometry, tractor fit, workload and willingness to pay.

**What if farms already own a sprayer?** A complete trailer can be harder to justify than a retrofit. Interview buyers about replacement cycles, retrofit demand and compatibility. A retrofit could become a separate product, but its price, costs and fit need their own model. Do not mix full-trailer costs with a retrofit selling price.

**Who are the competitors?** Properly calibrated conventional systems, canopy-sensing sprayers and existing intelligent products such as Smart Apply, which markets LiDAR-based vineyard control [S3]. We are proposing a focused RGB-camera, three-zone design. We have not proven lower cost, higher accuracy or better performance than incumbents.

**What is defensible?** Potential defensibility is vineyard-specific training data, verified calibration recipes, field reliability, serviceability and farm relationships. Three on/off nozzles alone are not a strong moat. No patent, exclusivity or freedom-to-operate clearance is claimed.

**Why now?** Our practical starting point is that the team has some cameras, tanks and spray components. The investment decision should rest on tested economics and field fit, rather than a claim that precision spraying is a new category.

## AI and engineering questions

**Where exactly is the AI?** A proposed foliage segmentation model distinguishes vine leaves from non-target pixels. Its output is summarized into visible occupancy scores for upper, middle and lower spray zones with a confidence measure. The controller uses those scores, speed and calibrated application recipes to schedule valve actions. It does not autonomously choose the chemical or invent a chemical dose.

**Why AI instead of “green means spray”?** A green threshold is a useful cheap baseline and might be sufficient in a controlled scene. A learned model could better distinguish vine foliage from weeds and background under difficult lighting. We must compare both on held-out vineyard rows and retain the learned approach only if it materially improves performance.

**How is canopy density calculated?** A first proxy is leaf pixels divided by valid pixels in each geometrically mapped zone. Visible occupancy is not leaf area index or full three-dimensional density; outer leaves hide inner leaves and fruit. Calibrate this proxy against actual canopy and deposition measurements. Multiple views or depth sensing may be needed.

**What data do you need?** Vineyard images from multiple farms, dates, cultivars, canopy stages, lighting conditions, weeds, dust and lens conditions. Annotate vine foliage versus other targets, occlusions and uncertain frames. Split training and test data by farm/row/date to prevent near-duplicate leakage. No labeled dataset or trained model has been provided yet.

**How would you measure the AI?** Segmentation IoU, foliage precision and recall, missed-target area, false activation in gaps, density error against a reference, end-to-end latency and uncertainty under adverse conditions. These perception metrics supplement actual spray deposition, delivered-volume error and crop outcomes; they do not replace them.

**How does the camera know when to spray?** Place it ahead of the nozzle line. Queue each target using measured ground speed and distance. Illustrative timing: 1 m of lookahead at 1.5 m/s gives 0.67 s travel time before subtracting valve and fluid delay. Recompute or track position as speed changes; stop spraying outside validated bounds. The render geometry is illustrative, not a dimensional design.

**Do the nozzles move?** No. The first concept uses three fixed directions, shown vertically stacked on one side pending team confirmation. Each has independent on/off control. Later two-sided coverage would need additional hardware and validation; do not claim it is already included in this first layout.

**Will all three have different pressures?** Not from a single unregulated common pressure line. A proposed first design holds manifold pressure within a calibrated band and controls individual output with compatible valves or PWM. True per-zone pressure control needs branch regulators and sensing. Pressure remains part of calibration and supervised control, but increasing pressure alone is not an adequate density strategy.

**Why not just increase pressure in dense vines?** Pressure changes flow and can change droplet behavior. For a fixed hydraulic nozzle, flow is approximately proportional to the square root of pressure: doubling flow can require roughly four times the pressure. Nozzle curves, product label, droplet requirements and deposition tests set the allowable range. Pressure is not proof of penetration. Dense grapes may need validated air assist or another delivery configuration; that could change the cost target.

**Will it use Wi-Fi or the cloud?** Proposed inference and control run locally. Internet access may help with updates and reporting but should not be required to spray. Report actual delivered flow as well as commands; valve-on time is not a reliable substitute for measured chemical application.

**Does it detect pests or disease?** Not in the initial scope. It detects intended foliage and estimates a density proxy. Disease-specific spraying is a possible later research direction, not a current capability. Fungicides often require preventive coverage even where no disease is visible.

**Can it spray herbicides too?** One chemical per operation is the plan, with label-required cleanout between products. Initial canopy targeting is for compatible insecticide/fungicide uses. Herbicides generally require distinguishing weeds from crop foliage and a separate target configuration; a green detector aimed at grape leaves must not be presented as a herbicide mode.

**What happens if it makes a mistake?** Proposed watchdogs close valves and alert the driver on stale frames, poor confidence, invalid speed or control faults. Headlands, stops and emergency-stop commands disable spraying. A measured-flow mismatch must trigger isolation and recovery. Any conventional fallback is deliberately selected by the operator using approved settings, not silently activated.

## Trial and acceptance plan

1. Audit actual tank, pump, valve, nozzle, camera and power specifications. Confirm row clearance, full-tank mass, towing geometry and service access.
2. Bench-test valve response, timing jitter, pressure stability when one or more valves close, leak behavior, flow measurement, electrical loss and emergency stop.
3. Use water-only trials to map visible occupancy to repeatable application recipes, and to measure gap shutoff distance and reactivation behavior. Calibrate the baseline sprayer properly.
4. Use replicated randomized or matched field blocks across canopy stages. Hold the comparison program, weather window and application conditions as consistent as possible; record departures.
5. Measure actual liters/acre and chemical amount/acre; deposition at top/middle/bottom, inner/outer and leaf undersides; target misses; off-target collectors; refill time; uptime; lens cleaning; valve faults and service cost.
6. Predefine an agronomist-approved coverage threshold and disease/pest non-inferiority margin. A suggested ≥20% eligible-volume reduction is a proposed economic target, not a safety or efficacy standard. Set sample size using variability and the agreed margin, rather than claiming one demonstration proves equivalence.
7. Monitor pest/disease incidence and severity through the spray program and season. Water-sensitive paper alone does not prove biological efficacy. A short water demo cannot validate seasonal protection.
8. Publish a farm-specific report, including failures and operating limits. Decide whether to release, revise or discontinue the design.

Draft sponsorship milestones: 40% on signed scope and component audit; 40% after bench/water acceptance; 20% after the agreed field acceptance or contract-defined remedy decision. Define title transfer, support hours, damage responsibility, data rights, chemical responsibility, farm access, budget overrun treatment and non-acceptance remedies before signing. Seasonal milestones depend on crop timing; a 90-day engineering phase is not a full-season efficacy promise.

## Claims to avoid

- “Our machine saves 73%.” The published 47–73% result is from a different laser-guided system in apple orchards [S1].
- “A visible cloud proves most pesticide is wasted.” A clip illustrates application and drift mechanisms; it does not quantify waste.
- “We eliminate drift” or “we spray only leaves.” Fixed cones can still send some spray through and around canopy, and sensor gating cannot eliminate wind effects.
- “AI directly measures all leaves” or “green detection guarantees crop protection.” It estimates a visible proxy.
- “Zero crop damage,” “fully autonomous,” “patented,” “EPA-approved,” “signed farm partners,” or “production ready.” None has been established.
- “Compatible with every pesticide.” Product labels and local requirements determine allowed uses, application volumes, rates and operating conditions [S4].

## Open facts to confirm with the team

Product and team name; location and currency; pitch time limit; judging format; vertical or other zone arrangement; one- or two-sided first unit; exact hardware specifications; prototype integration status; engineering/fabrication/AI/agronomy roles; available sponsor relationships; actual budget; willingness to offer two units; and whether tomorrow's presentation has internet and PowerPoint video playback.

## Sources

- **S1 — USDA ARS / Chen et al., 2013:** [Spray drift and off-target loss reduction with a precision air-assisted sprayer](https://www.ars.usda.gov/research/publications/publication/?seqNo115=296307). Apple-orchard laser-guided study, not a grape-camera prototype result. Reported spray-volume reduction 47–73%, with comparable inside-canopy deposition quality.
- **S2 — USDA NASS:** [Noncitrus Fruits and Nuts 2025 Summary, p. 38](https://release.nass.usda.gov/reports/ncit0526.pdf). Reports 883,000 U.S. grape bearing acres for 2025. Annual reported-state coverage is not every vineyard or all bearing/nonbearing census acreage.
- **S3 — Smart Apply:** [Vineyard product description](https://www.smartapply.com/growers/vineyards). Vendor-described LiDAR system; vendor claims are not independent comparative results for this project.
- **S4 — U.S. EPA:** [Introduction to Pesticide Labels](https://www.epa.gov/pesticide-labels/introduction-pesticide-labels). Labels govern legally allowed application.
- **S5 — Virginia Tech / Douglas G. Pfeiffer:** [Airblast calibration laboratory](https://www.virginiafruit.ento.vt.edu/airdemo.html). Source of the attributed water-only orchard clip; the lab demonstrates coverage tradeoffs, not proof of needless excess.
- **S6 — OMAFA / CropLife Canada, via Sprayers 101:** [Spray drift education videos](https://sprayers101.com/omafra-drift-video/). Additional linked drift footage; online playback was unavailable in the research environment.
- **S7 — Health Canada:** [Management of Pesticide Spray Drift](https://www.canada.ca/en/health-canada/services/consumer-product-safety/pesticides-pest-management/growers-commercial-users/drift-mitigation/management-pesticide-spray-drift.html). Describes airblast configurations, airflow and off-target deposition mechanisms. Use local requirements for the actual pilot.
