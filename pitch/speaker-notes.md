# CanopyFlow — five-minute speaker script

Working name and all proposed financial terms are editable. Slides 1–12 are the pitch; later slides are Q&A backup. Timing includes short media playback.

## 1. Every gap is a chance to save.

[0:00–0:20] Every gap in a vine canopy is a chance to save spray. We are developing CanopyFlow: a tractor-towed sprayer that sees foliage and matches output to the plant target. We are seeking a farm partner to prove the savings without compromising crop protection.

## 2. Spraying empty space still costs money.

[0:20–0:45, including 8-second clip] Constant output can spray through canopy gaps. [Play clip.] This university water-only orchard demonstration illustrates the need to match application to the target. It is not our machine, grape footage or a measurement of waste.

## 3. Keep the tractor. Make the spray respond.

[0:45–1:10, including 8-second animation] Our proposed trailer combines a single tank, cameras and three fixed spray zones. [Play animation.] Each zone switches independently; the nozzles do not move. This original concept animation uses synthetic canopy states, not live AI or prototype test results.

## 4. A canopy map becomes a timed spray decision.

[1:10–1:40] The proposed AI separates vine foliage from background and estimates visible density in upper, middle and lower zones. The controller uses ground speed and camera lookahead to time each valve. Gaps switch off; foliage receives calibrated output. We will compare learned segmentation against simple green detection. The AI must add measurable value under shadows, weeds and changing light. Control runs locally.

## 5. The buyer needs a payback case.

[1:40–2:10] Here is an illustrative business case, not a result. One unit serves 500 unique acres with 250 dollars per acre in annual eligible chemicals. A 30 percent reduction saves 37,500 dollars. After 1,500 dollars of annual upkeep, net savings are 36,000 dollars. At a proposed 24,000-dollar purchase price, simple payback is 0.67 years. Smaller savings can make payback much longer.

## 6. Start where repeated applications matter.

[2:10–2:30] Our first customers are large vineyards and custom applicators. USDA reports 883,000 U.S. grape bearing acres for 2025. Our reachable-acre scenario is an assumption, not a customer count. We will establish actual demand through local interviews, equipment-fit checks and pilot conversion.

## 7. Precision spraying is a proven category.

[2:30–2:55] Precision spraying already exists. Smart Apply markets LiDAR-based vineyard control, and well-calibrated conventional sprayers are also competitors. Our proposed difference is a focused camera-based, three-zone design. We must demonstrate competitive installed cost, serviceability and coverage. We are not yet claiming lower cost or better performance than existing products.

## 8. Sell equipment. Earn the next deployment.

[2:55–3:20] The proposed complete trailer sells for 24,000 dollars, excluding the tractor. Our estimated build-and-delivery cost is 14,000 dollars, leaving 10,000 dollars gross profit before overhead and research. Those are planning assumptions awaiting quotes. We would start with direct farm sales and local service, then expand through referrals and dealers.

## 9. Fund a pilot. Receive two units.

[3:20–3:45] We propose a 60,000-dollar founding-farm sponsorship. The farm receives two included pilot units after agreed acceptance, defined support and a results report. Funding covers the builds, engineering, validation and contingency. The farm contributes trial access and operational records. Milestones and remedies must be agreed; this is development sponsorship, not guaranteed savings.

## 10. Lower use only counts if protection holds.

[3:45–4:15] Lower use only counts if protection holds. We start with bench and water tests, then replicated comparisons against a calibrated baseline. We measure actual chemical use, inside-canopy coverage, reliability and seasonal pest or disease outcomes. Our proposed target is at least 20 percent less eligible spray volume, with agronomist-approved protection criteria. Product labels govern application. Faults stop automated spraying and alert the driver.

## 11. Hardware on hand. Integration comes next.

[4:15–4:40] We already have some cameras, tanks and spray hardware. The next step is integration, not a production-readiness claim. A proposed first 90 days covers the component audit, controller and water testing; seasonal trials follow the crop calendar. We still need confirmed engineering roles, hardware specifications and a host farm.

## 12. Help us prove the savings in your vineyard.

[4:40–5:00] We are seeking one founding farm for a milestone-based pilot: two units and a measured decision about deployment. CanopyFlow aims to spend less spray on gaps and match output to the crop. Help us prove the savings in your vineyard.

## 13. What if savings are smaller?

All scenarios are illustrative and assume unchanged eligible treatment program and acceptable crop protection. Acres are unique annual acres served, not acres multiplied by passes. Cost per acre is annual eligible chemical product cost across those passes. Savings percentage is a reduction in chemical product use/cost at unchanged unit price, not just a reduction in water. Zero or negative net savings means no simple payback.

## 14. A complete-unit cost target—not supplier quotes.

Estimated unit build cost: chassis and tank 3,500; pump, plumbing and three-zone valves 2,500; cameras and edge compute 1,500; power, sensors and enclosure 1,200; fabrication and assembly 3,000; delivery, installation and initial warranty reserve 2,300. Total 14,000 dollars. Existing components need inventory and replacement-value confirmation. No supplier quotations obtained. Cost target may change if air assist, greater throughput or two-sided coverage is required. Pilot budget is separate from a sale-price scenario.

## 15. Density informs flow; pressure needs limits.

Pressure and flow are coupled. For a fixed hydraulic nozzle, flow is approximately proportional to the square root of pressure, so doubling flow can require roughly quadrupling pressure. Use nozzle-specific curves, calibrated recipes and pressure limits. A shared pump can hold a regulated pressure while individual compatible valves or PWM set zone output. If true independent pressures are necessary, add regulators and sensors per branch. Visible foliage occupancy is not full canopy density; multi-view sensing or depth may be needed. Lookahead delay is distance divided by speed, minus measured actuation and fluid delays. Example: 1 meter lookahead at 1.5 meters per second is 0.67 seconds before subtracting delay. Reject out-of-range speed or insufficient lookahead. No actual pressure setpoints are proposed without the nozzle and product label.

## 16. The driver remains in control.

Planned controls, not implemented results: low-confidence image, obscured lens or stale frames stop automated spraying and alert the driver; any return to a calibrated conventional mode requires deliberate operator action and approved settings. Low or high flow, pressure loss and stuck-open valve require monitored shutdown and isolation. Headlands and stopped tractor close valves. Validate command watchdog, electrical loss, speed bounds and emergency stop. Keep records of actual delivered flow, not just commanded valve state. Green weeds behind the vines require segmentation, geometry and confidence checks. Herbicide use must not reuse crop-canopy targeting.

## 17. What is sourced—and what is still a hypothesis?

USDA ARS Chen et al. 2013 studied a laser-guided variable-rate sprayer in an apple orchard, not our RGB-camera design in grapes. It reported 47–73 percent spray-volume reduction versus a constant-rate comparison with comparable inside-canopy deposition quality. Do not present the upper bound as our expected savings. Our 30 percent base-case chemical-cost reduction is a planning assumption. Actual savings depend on label-consistent application, concentration, crop stage, gaps, coverage, climate and equipment. NASS acreage is reported crop context, not a customer count. Smart Apply information is vendor-stated competitive context.

## 18. Source links for judge questions.

Links checked through source pages during preparation. Some embedded video hosts could not be played from the research environment. See media-cues.md for playback status and fallback narration. Research prepared November 14, 2026, America/Los_Angeles.

## 19. Source links for judge questions.

Links checked through source pages during preparation. Some embedded video hosts could not be played from the research environment. See media-cues.md for playback status and fallback narration. Research prepared November 14, 2026, America/Los_Angeles.