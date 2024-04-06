- Resume
	- The paper proposes the use of a hybrid approach to low cost/power devices for the TOCTOU (Time Of Check, Time of Use) attacks. This approach is basically a timestamp/counter for the last time a write operation (modifiication) of the attested region was performed. If the time stamp is different than the one on the verifier the device has been compromised.ç
	- RA serves as a foundation for many security services, such as proofs of memory erasure, system reset, software update, and verification of runtime properties. Prior RA techniques verify the remote device binary at the time when RA functionality is executed, thus providing no information about the device binary before current RA execution or between consecutive RA executions. This implies that presence of transient malware (in the form of modified binary) may be undetected. In other words, if transient malware infects a device (by modifying its binary), performs its nefarious tasks, and erases itself before the next attestation, its temporary presence will not be detected.
	- This important problem, called Time-Of-Check-Time-Of-Use (TOCTOU), is well-known in the research literature and remains unaddressed in the context of hybrid RA.
	- In this work, we propose Remote Attestation with TOCTOU Avoidance (RATA): a provably secure approach to address the RA TOCTOU problem. With RATA, even malware that erases it- self before execution of the next RA, can not hide its ephemeral presence.RATAtargetshybridRAarchitectures,whichareaimedat low-end embedded devices. We present two variants – RAT AA and RATAB – suitable for devices with and without real-time clocks, respectively
		- demonstrates low hardware overhead of both techniques. Compared with current hybrid RA architectures – that offer no TOC- TOU protection – RATA incurs no extra runtime overhead.
- Interesting methods
	- They use a MSP430 RTL to simulate and add custom HW to the device to monitor/control the access entries on the attested region
- This paper is centered around a witness for modifications on the attested regions, meaning this a software attestation and not a CF attestation as the one w
-