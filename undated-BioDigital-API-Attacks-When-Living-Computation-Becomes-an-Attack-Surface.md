---
title: "BioDigital API Attacks: When Living Computation Becomes an Attack Surface"
date: undated
source: LinkedIn Articles
author: Divyendu Bhatt
---

# BioDigital API Attacks: When Living Computation Becomes an Attack Surface

![](https://media.licdn.com/mediaD5612AQGRpJQI-FxPWQ)

# [BioDigital API Attacks: When Living Computation Becomes an Attack Surface](https://www.linkedin.com/pulse/biodigital-api-attacks-when-living-computation-becomes-dm-bhatt-hzkhc)

Created on 2026-10-21 02:07

Published on 2026-10-21 02:36

<div>

*By Divyendu Bhatt*

Cybersecurity must prepare for systems in which software interacts with living biological computation. Wetware, Synthetic Biological Intelligence (SBI), and organoid intelligence introduce a boundary where digital instructions can influence biological activity—and biological responses can influence digital decisions.

This boundary is already becoming programmable. Cortical Labs’ CL API enables real-time, closed-loop interactions with biological neural networks. FinalSpark’s published Neuroplatform research describes remote access to neuronal cultures through a Python API. These developments establish a foundation for remotely accessible biological computation; they do not establish that these platforms have suffered biological computing attacks.

As this field develops, cybersecurity must examine what happens when compromised identities, software, or automated agents gain access to that boundary.

### Introducing BioDigital API Attack "BDAA"

**I propose the term BioDigital API Attack (BDAA)** to describe:

> An adversarial action through a programmable interface connecting digital systems and living biological computation, intended to compromise biological inputs, adaptive states, measured outputs, or downstream decisions.

The defining characteristic is interference across the digital–biological trust boundary. A breach of a biocomputing provider’s billing system would remain a conventional cyberattack. An intrusion that manipulates signals delivered to biological computation, falsifies its readouts, or corrupts its feedback loop would fall within this proposed BDAA definition.

### A Future Scenario: Wetware as a Service Goes Wrong

Imagine a research organisation renting access to living neural networks through a cloud service. Researchers submit experiments through Python notebooks. AI agents coordinate workflows, analyse biological responses, and recommend subsequent experiments.

Now imagine that a researcher’s service account is compromised.

The attacker appears to be an authorised user. Excessive permissions in this hypothetical service allow that account to alter experimental workflows, manipulate feedback, and interfere with recorded results.

The first symptom is subtle: experiments become less reproducible. Measurements remain plausible, but their interpretation has been altered. An automated research agent accepts the compromised evidence and uses it to recommend further experiments.

The organisation now faces three questions:

-   Were the experimental records manipulated?

-   Was the biological system itself influenced?

-   Which downstream conclusions can still be trusted?

A conventional identity compromise has crossed into a BioDigital API Attack. Its consequences could include invalid experiments, wasted research effort, misleading conclusions, and potentially unsafe downstream actions where independent controls are absent.

This is a hypothetical scenario, not a description of a known compromise of current wetware platforms.

### The Connection to Present-Day Incidents

The Novo Nordisk incident provides a relevant comparison at the digital infrastructure layer. The company disclosed unauthorised access to internal IT systems and external copying of non-public information, including personal data. Its update described exposure of certain pseudonymised clinical-trial information and stated that core business operations remained operational. The disclosure does not establish manipulation of experiments, biological systems, or wetware.

The connection is architectural: life-sciences research already depends on digital identities, software, and information systems. As biological experimentation becomes remotely programmable, a future compromise could potentially extend from accessing research records to interfering with how experimental evidence is generated.

**The emerging concern is the progression from stealing biological information to compromising the integrity of biological computation.**

### Potential Future BDAA Scenarios

Under this proposed terminology, the attack surface could include:

-   **Biological input manipulation:** unauthorised alteration of signals delivered to living computational systems.

-   **Adaptive-state poisoning:** manipulation of feedback intended to influence learning and subsequent behaviour.

-   **Biological readout falsification:** tampering with recorded activity or its interpretation.

-   **Feedback-loop hijacking:** compromising the loop connecting biological responses and digital instructions.

-   **Biological resource exhaustion:** abusive workloads that threaten service availability or biological viability.

-   **Downstream authority abuse:** exploiting software that grants excessive execution authority to biological computational outputs.

These are prospective threat scenarios requiring research and validation, rather than established vulnerabilities across current platforms.

### Why Recovery Could Be Different

Defenders can revoke credentials, isolate services, and restore software. But if an attack has influenced an adaptive biological system, another question arises: **has that system returned to an acceptable experimental baseline?**

Whether malicious feedback could produce persistent, security-relevant biological changes and how reliably those changes could be detected or reversed remains a research question. Natural biological variability would complicate attribution: an unusual response alone would not prove an attack.

Even without persistent biological changes, falsified measurements could contaminate downstream analysis. Recovery would therefore need to establish which experiments, observations, and conclusions remain trustworthy.

### Towards BioDigital Security Operations Centres

For defence, I propose exploring **BioDigital Security Operations Centres (BSOCs)**: an operating model combining cybersecurity monitoring, biological-state observation, instrumentation integrity, experimental provenance, and safety oversight.

Such a capability would correlate identity activity and API actions with instrument telemetry, biological observations, and downstream decisions. Its purpose would be to detect unauthorised interactions and help establish whether experimental evidence remains reliable.

Present documentation already recognises the need for strong controls. FinalSpark’s SDK guidance treats hardware-changing tools as privileged and recommends bounded inputs, human approval, structured logging, and safe cleanup when connecting them to AI agents. These are relevant safeguards, not evidence of a breach.

**BDAA names the proposed attack class. BSOC names a proposed defensive capability.** Both require measurable controls and experimental validation.

When computation becomes biological, incident recovery may require more than restoring systems. It may require re-establishing trust in the experiment itself.

**When software can influence living computation, how do we establish and continuously verify trust across that boundary?**

\#BioDigitalAPIAttack \#BDAA \#BioDigitalSecurity \#Wetware \#SyntheticBiologicalIntelligence \#OrganoidIntelligence \#Biocomputing \#CyberBiosecurity \#FutureOfCybersecurity \#EmergingThreats \#ZeroTrust \#BSOC

</div>