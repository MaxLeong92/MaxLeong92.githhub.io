# MaxLeong92.githhub.io
May 19, 2026
DTG / Efalke Engineerig Call
Invited mdurica@efalke.com Dave Pasko fpaparella@efalke.com David Sevigny Rob Marvin malmufti@efalke.com eespina@efalke.com
Attachments DTG / Efalke Engineerig Call


Summary
Technical issues analysis and safety risks highlighted production timeline concerns for the project.

Battery and Fault Investigation
Teams investigated battery detection errors and potential safety hazards regarding high voltage capacitors. Testing protocols were prioritized to mitigate damage risks.

Display Software and Hardware
Participants approved programming the Liquid Crystal Display chips directly to bypass case accessibility constraints. Validation will proceed despite unit damage risks.

Resource Allocation and Timeline
Management determined that the current production timeline is unfeasible due to critical system bottlenecks. Resources will be reallocated to separate charger and controller tasks.

Rate this Summary: Helpful or Not Helpful


Decisions
We've updated the Decisions section using your feedback.
Let us know what you think: Helpful or Not Helpful

ALIGNED
●	Battery testing safety protocol Battery testing and movement are suspended for existing units until the engineering team provides specific guidance on preventing hardware damage.
●	Manual display firmware programming The team will utilize the STM programmer to update display firmware by opening the unit to access the header, accepting that this process will damage the glued casing.
●	Production timeline re-evaluation The engineering team will conduct an internal assessment of outstanding technical issues to provide a realistic update to the production timeline.


Next steps
	[Evan Espina] Battery Testing Protocol: Consult with Milan to define dos and donts for the remaining 3 batteries to prevent damage. Report back to the team immediately.
	[Rob Marvin] Halt Battery Testing: Keep batteries in their current configuration until receiving guidance on safe handling procedures.
	[Evan Espina] Share Fault List: Send the description list regarding the fault and state information to Anthony.
	[Evan Espina] Provide Programming Details: Share the location of the programming header and connector for the display chip with the team.
	[Evan Espina] Analyze Controller Failure: Collaborate with Fran to replicate issue 32 on the test bench to identify root causes.
	[Rob Marvin] Upload Serial Data: Upload the serial data dump file for the controller failure to the relevant issue folder.
	[Evan Espina] Resolve Charger Issues: Investigate root causes for charger freezing issues 20 and 30 on the test bench.
	[Evan Espina] Update Project Timeline: Assess internal resource availability for charger issue resolution and provide updated production timelines to the team.
	[Evan Espina] Share Efficiency Reports: Deliver internal inverter efficiency test reports and methodology details to the team.


Details
●	Battery Detection Issue and Risk Mitigation: Evan Espina reported that the team is investigating a "battery not detected" issue, suspecting a resistor that requires an increased power rating. The team is attempting to replicate this issue to confirm if the resistor change resolves it, with further updates expected by the next Tuesday meeting. David Sevigny expressed concern regarding the safety of the three remaining good batteries during testing. Consequently, Evan Espina committed to verifying proper handling procedures with Milan, and David Sevigny instructed Rob Marvin to maintain the current battery placement until further guidance is provided.
●	Fault and State Information: There was a request for a description regarding fault and state codes. Evan Espina is working to obtain this list from the software engineer and intends to share it by the end of the day or the following morning.
●	Software Updates for the Liquid Crystal Display: The team discussed the difficulty of performing software updates on the current Liquid Crystal Display units due to the inability to access internal components without breaking the glued, 3D-printed cases. Dave Pasko noted that they possess STMicroelectronics programmers and could program the chips directly if the necessary header information was provided. Evan Espina agreed to provide the specifications for the programming header and the probe locations on the board, allowing the team to proceed with validation despite the risk of damaging a unit.
●	Unit Tear-Down Analysis and Safety: Dave Pasko explained that they performed a tear-down analysis on one unit to understand the internal assembly, as the system is often treated as a "black box" and they need to serve as the first line of defense for customer issues. mohammed ghazwan cautioned that the Uninterruptible Power Supply contains Alternating Current and high-voltage Direct Current capacitors, which pose significant safety risks even when the unit is not operating, and requested that the team handle these components with extreme care.
●	System Controller Failure (Issue 32): The team addressed a major failure labeled as Issue 32, where a unit became unresponsive, exhibiting alternating flashing lights and an inability to reboot. This failure occurred following Issue 31 on the same unit. Evan Espina stated that Fran would review the associated videos and diagnostics, while Rob Marvin agreed to provide a serial data dump from the unit to assist in the investigation.
●	Charger Freezing Issues: Dave Pasko and Rob Marvin reported that the charger frequently freezes, requiring a power cycle to recover, even when no batteries are connected. Evan Espina acknowledged the issue and stated that after making progress on the controller-related issues, they will have Fran examine the charger software.
●	Production Timeline and Resource Allocation: David Sevigny raised concerns regarding the feasibility of the June to August production timeline given the number of significant, unresolved bugs. Evan Espina noted that the same team is currently handling both the charger and controller issues, creating a bottleneck. The team agreed to evaluate current resources and internal knowledge transfer to determine if tasks could be separated to improve efficiency. The participants committed to refining these timelines and providing realistic updates to the operations team to avoid last-minute delays.
●	Inverter Efficiency Testing: Dave Pasko requested the existing inverter efficiency test data and the associated test conditions to ensure they can replicate results and communicate accurate performance metrics to customers. Evan Espina added this to their list and committed to reaching out to the internal team to retrieve the relevant reports.


You should review Gemini's notes to make sure they're accurate. Get tips and learn how Gemini takes notes
How is the quality of these specific notes? Take a short survey to let us know your feedback, including how helpful the notes were for your needs.

Jun 2, 2026
DTG / Efalke Engineerig Call
Invited mdurica@efalke.com Dave Pasko fpaparella@efalke.com David Sevigny Rob Marvin malmufti@efalke.com eespina@efalke.com
Attachments DTG / Efalke Engineerig Call


Summary
Technical teams reviewed testing updates and adjusted protection limits while confirming production schedule stability.

Battery Certification And Software
Battery certification remains delayed, yet design changes will not disrupt the overall production schedule. Software issues regarding power delivery and fault reporting have been resolved.

Thermal Testing And Protection
Engineers increased the over-temperature protection set point to 115°C to ensure safety during high-temperature operations. Testing continues to confirm performance within real-world environments.

Production Updates And Documentation
Upcoming units include improved programming capabilities, while cosmetic issues are slated for correction in future batches. Documentation will be updated to reflect specific inverter capacity requirements.

Rate this Summary: Helpful or Not Helpful


Decisions
NEEDS FURTHER DISCUSSION
●	Thermal interface material selection pending Testing will be conducted to evaluate thermal performance and costs to determine the necessity of thermal gap pads versus metal-to-metal contact for controller mounting.

ALIGNED
●	Parallel production schedule maintained The production schedule will proceed in parallel despite battery certification delays, as the current battery samples maintain the same configuration as the certified version.
●	OTP set point increased to 115°C The Over-Temperature Protection (OTP) set point is increased to 115°C for the transformer and the backup charger to resolve identified thermal issues.
●	Testing documentation includes battery caveat The testing procedures document will include a caveat specifying that inverter test settings assume a minimum 1500 watt-hour fixed battery configuration.

We've updated the Decisions section using your feedback.
Let us know what you think: Helpful or Not Helpful


Next steps
	[mohammed ghazwan] Verify Schedule: Verify if the project schedule has been updated to reflect battery certification delays.
	[EVO] Update Report: Update the safety report for issue 22 with the latest test data regarding Over Temperature Protection set points.
	[Rob] Reproduce Error: Attempt to reproduce the battery error 1 on the current setup.
	[EVO] Prepare Report: Draft a summary covering issues 21 and 22 following the software change.
	[Evan Espina] Finalize Units Plan: Determine the resolution plan for the 5 systems on hand and notify the team via email or WhatsApp.
	[Rob] Source Thermal Pads: Research and procure options for thermal gap pads for cart controller installation.
	[Rob] Test USB Connectivity: Re-verify power connectivity to confirm functionality across all voltages.
	[Rob] Record Serial Video: Provide a video of the serial line output to help debug power issues.
	[Dave Pasko, Rob] Review Cable Pinout: Review pin configurations to determine how to fabricate the necessary programming interface.
	[Luan] Coordinate Issue Reproduction: Reach out to Rob directly to coordinate the reproduction of outstanding items.
	[Rob, Francesco Paparella] Troubleshoot Display Power: Collaborate to investigate and resolve display power connection issues.
	[Evan Espina] Record Stress Videos: Create clips documenting the stress test setup used on the workbench.
	[Evan Espina] Confirm Spare Latches: Check the inventory count of available spare CNC latches for shipment.
	[Rob] Update Test Documentation: Include a table specifying wattage requirements for each product model.


Details
●	Safe Tech Report and Battery Certification Status: Dave Pasko inquired about the status of the Safe Tech report and battery certification, which were previously due in the third week of May. Mohammed Ghazwan explained that certification is delayed because of required changes to the battery design, necessitating new samples and testing, and the schedule is not yet updated to reflect this.
●	Impact of Battery Changes on Schedule: Mohammed Ghazwan and David Sevigny discussed the impact of the battery design changes. It was established that these changes will not impact the overall production schedule because work can proceed in parallel, and the samples provided will be of the same configuration as the version submitted for certification.
●	Software Fix for Issue #23: Evan Espina reported that the software fix for issue number 23 has been completed and tested successfully. Evo is responsible for updating the report with this information.
●	Overheat Fault Testing (Issue #22): Evan Espina detailed testing for the overheat fault, which involved back-to-back discharge cycles. Results showed temperatures reaching 83°C at ambient temperature and slightly over 105°C at 40°C ambient. The team decided to increase the over-temperature protection (OTP) set point to 115°C, which provides a margin against the 145°C limit specified in the safety report. Evo will update the report with this test data.
●	BB Charger Over-Temperature Protection (Issue #21): Evan Espina identified that error number one is caused by the backup charger (BB charger) OTP tripping. The NTC for the BB charger is located near the transformer being tested for issue 22, causing it to heat up even when not charging. The team will increase the BB charger OTP set point to 115°C, and Evo will prepare a report covering both issues.
●	Bench Versus Cart Testing: David Sevigny expressed concerns regarding the thermal testing, noting that bench tests may not accurately reflect heat dissipation within the tech tray of a warehouse cart. Evan Espina confirmed that the 115°C OTP limit is based on a 40°C ambient environment, and Mohammed Ghazwan noted that the cart's metal base might facilitate better thermal transfer, though testing within the cart is still required to confirm performance.
●	Repair Plan for Existing Systems: David Sevigny inquired about the plan for the five existing systems on hand. Evan Espina stated that the team will evaluate the effort required and determine whether the systems should be repaired in-house or shipped back for service, with an answer expected by the next meeting.
●	Controller Mounting Thermal Material: Rob Marvin asked if thermal gap pads are necessary between the controller and the cart. Evan Espina indicated that while gap pads are recommended, they must be weighed against cost and available space. David Sevigny suggested they will test the performance first before deciding on a permanent solution.
●	USB Power Issue (#37): Evan Espina reported that the USB power issue for 5V, 9V, 12V, 15V, and 20V is resolved via a software update, allowing the delivery of 3 amps. Francesco Paparella clarified that the inverter must be turned on via the display, not the switch, to allow USB power. Rob Marvin will re-test this configuration, and Francesco Paparella requested a video of the terminal serial line if issues persist.
●	LCD Serial Data Access: Mohammed Ghazwan and Francesco Paparella discussed using Y-cables to retrieve data from the UPS while the LCD is connected. Francesco Paparella confirmed this method works, allowing them to read serial data on a laptop while simultaneously viewing the display.
●	ST Programming Tools: Dave Pasko and Francesco Paparella discussed the incompatibility of the programmer model requested by the team. Dave Pasko has a newer programmer model and will coordinate with Rob Marvin to review the pinouts and create a custom cable to allow programming on-site.
●	Display Bootloader Capability: Evan Espina announced that the next two units will feature bootloader capability, allowing for future software updates to the display on-site. The team will provide guidelines for this process, and existing units can be flashed once the programmer is ready.
●	Handling Unreplicated Issues: David Sevigny requested updates on issues the engineering team has been unable to replicate. Evan Espina agreed to coordinate with Luan, the engineer assigned to these tasks, to identify which items are pending and to have Luan contact Rob Marvin directly for collaboration.
●	Battery Handle Cosmetic Issue (#38): David Sevigny raised a concern regarding plastic depressions on the battery handles. Mohammed Ghazwan confirmed this is known and will be addressed in the next production batch of plastic parts, which will be monitored by an engineer at the supplier site. Samples with the corrected texture and logo will be sent once available.
●	CNC Latch Samples: Mohammed Ghazwan and Evan Espina confirmed that CNC latch samples will be included in the next shipment of units.
●	Documentation of Stress Testing: David Sevigny requested video documentation of the abusive stress testing performed on the latches to ensure internal testing standards align with the supplier's definition of durability. Evan Espina agreed to coordinate this with Mohammed Ghazwan offline.
●	Serial Connection Troubleshooting: Rob Marvin reported difficulties maintaining a stable serial connection to controllers. Evan Espina and Francesco Paparella suggested that the issue is likely related to the quality of the provided cables or connection stability and advised Rob Marvin to contact Francesco Paparella directly to troubleshoot or share a video of the setup.
●	Shipment of Next Samples: Evan Espina confirmed that the team is preparing two sets of UPS units, displays, and batteries for shipment. Regarding the outstanding units, Evan Espina indicated that the instruction from Yoken is to provide two sets, and inquiries regarding the full quantity of ten should be directed to Yoken and Steve.
●	Testing Documentation and Battery Compatibility: Rob Marvin discussed plans to update the testing documentation to specify clear procedures for different inverter wattages (300W, 1000W, and 1500W-2000W). They noted that these settings assume a minimum 1500Wh fixed battery capacity to prevent overloading, and the documentation will be updated to include this caveat.


You should review Gemini's notes to make sure they're accurate. Get tips and learn how Gemini takes notes
How is the quality of these specific notes? Take a short survey to let us know your feedback, including how helpful the notes were for your needs.

Jun 9, 2026
DTG / Efalke Engineerig Call
Invited mdurica@efalke.com Dave Pasko fpaparella@efalke.com David Sevigny Rob Marvin malmufti@efalke.com eespina@efalke.com
Attachments DTG / Efalke Engineerig Call


Summary
Meeting discussions prioritized battery testing protocols and documentation requirements while aligning on current hardware and charger status updates.

Battery Validation and Issues
Teams addressed battery connection failures by refining resistor values and planning comprehensive cycling tests. Data transparency regarding cycle counts will ensure solution reliability.

Documentation and Reporting Standards
Stakeholders decided to produce a detailed acceptance report to verify issue resolution rather than simple status flags. The team also committed to updating the project tracker with accurate statuses.

Hardware and Logistics Planning
Engineering confirmed charger issues require higher prioritization for production. The team aligned on shipment paperwork processes and obtaining necessary binary files for chip programming.


Decisions
Aligned
●	Battery shipment delayed until next Tuesday The shipment of assembled batteries is delayed until next Tuesday to allow for additional qualification and cycle testing.
●	Acceptance report required prior to shipment An acceptance report detailing quality verification tests must be provided and approved by DTG as a requirement before products can be shipped.

We've updated the Decisions section using your feedback.
Let us know what you think: Helpful or Not Helpful


Next steps
	[Rob] Send BMS Address: Provide the address for damaged BMS boards to the team.
	[Evan] Send Shipment Paperwork: Send shipment initialization paperwork to initiate the process with the logistics company.
	[The group] Follow Up Shipment: Follow up with the shipment company to finalize the logistics documentation.
	[Evan] Create Acceptance Report: Compile an acceptance report list detailing the validation status of batteries and USB power components.
	[Milan] Draft Hot Swap Plan: Draft a hot swap test plan for the battery hardware.
	[Evan] Draft Cycle Test Plan: Draft a charge and discharge cycle test plan for battery qualification.
	[Evan] Share Test Plans: Share the finalized test plans for battery and USB power validation with the team.
	[Rob] Request Binary File: Request the ST chip binary file from Fran.
	[Rob] Flash ST Chip: Flash the ST chip using the provided binary file.
	[Evan] Update Battery Report: Update the acceptance test report for the battery component.
	[Francesco and Yoken] Provide USB Report: Provide the USB power acceptance test report.
	[Evan] Update Charger Status: Provide a comprehensive status update on charger mechanical and electrical issues.


Details
●	LCD and Controller Wiring Status: Rob Marvin reported receiving the programmer and cables but stated they have not yet performed the wiring, noting that the team is currently awaiting new displays and controllers. Dave Pasko clarified that the priority of this task relates to assessing new LCD functionality, but the team is currently waiting for new hardware. Rob Marvin explained that they were previously instructed to set aside testing on older equipment to focus on Amazon site visits and photo organization, so this task is currently on hold. Dave Pasko suggested that they may revisit this work on the 22nd or 23rd.
●	Battery Connection Issue and Testing Timeline: Evan Espina provided an update on the battery connection issue, stating that two new batteries have been assembled with fine-tuned resistor values to resolve the problem. The team plans to conduct cycling tests on Wednesday and Thursday, with a potential shipment date of next Tuesday to allow for sufficient qualification time rather than rushing a Friday shipment. The uninterruptible power supply (UPS) is already prepared, making these batteries the final outstanding items.
●	Battery Test Validation and Data Requests: David Sevigny expressed concern regarding the validity of the battery fix, citing previous instances where batteries failed even after initial testing. David Sevigny requested specific data on the number of cycles and insertions performed, rather than just the number of days spent testing, to ensure confidence in the solution. Evan Espina agreed to share a summary of the test plan, covering hot swap and charge/discharge cycle details, to demonstrate the rigor of their validation process.
●	Damaged Battery Management System Boards: Evan Espina and Rob Marvin discussed the return of damaged Battery Management System (BMS) boards. Rob Marvin confirmed receiving the shipping address in a text message and will arrange the return, which Evan Espina noted will help verify the hypothesized root cause of the connection failures.
●	USB Power Qualification and Reporting: Evan Espina reported that the USB power functionality is operational, but further qualification testing is required, specifically regarding constant power (CP) load recovery and overload conditions. There are pending 80 reports regarding the USB power system that need to be finalized and shared with DTG.
●	ST Chip Programming and Shipment Paperwork: Evan Espina instructed Rob Marvin to contact Fran to receive the binary file necessary to flash the ST chip. Regarding shipment logistics, Evan Espina planned to initiate the notification, and David Sevigny advised that relevant paperwork should be directed to Corey and Adam via the existing email thread from the previous Friday.
●	Acceptance Report Requirements: David Sevigny emphasized the necessity of a high-level acceptance report that details the specific tests conducted to confirm that issues are resolved rather than just marking items as "green". Mohammed Ghazwan agreed, suggesting the report include results from specialized cycle testing and documentation of the specific fixes implemented to resolve issues identified by DTG. Evan Espina committed to working with the team to prepare this documentation.
●	Project Tracker Status: Dave Pasko noted that the project tracker on SharePoint appears outdated, with no entries since June 4th. Evan Espina clarified that a separate, updated tracker exists for the current battery sets and agreed to update the main tracker to reflect "done" statuses, which indicate that the next shipment of hardware or software will address those specific issues. The team resolved confusion regarding hidden cells in the tracker that had obscured completed items.
●	Unresolved Project Issues: David Sevigny noted that several items on the tracker remain open because they have not been reproducible. David Sevigny offered Rob Marvin’s availability to help the engineering team witness and troubleshoot these issues before the product is finalized for shipment.
●	Charger Status and Criticality: David Sevigny raised concerns about the charger, noting that it is critical for production even though it currently holds a lower priority than the batteries and controllers. Evan Espina confirmed there are two electrical issues and two mechanical issues under investigation, with the main mechanical concern involving tolerances in the metal case. Evan Espina agreed to provide a separate update on the charger status and to increase the priority of the electrical issues to ensure they align with the production timeline.


You should review Gemini's notes to make sure they're accurate. Get tips and learn how Gemini takes notes
How is the quality of these specific notes? Take a short survey to let us know your feedback, including how helpful the notes were for your needs.
