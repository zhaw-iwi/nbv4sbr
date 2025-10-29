# Non-Verbal Behaviour Vocabulary (NBV) for Robotic Social Behaviour Regulation
This project aims to bridge HCI, performance studies, and embodied AI to advance reproducible, socially aware robot behaviour.

### Why
Social interaction involves far more than words.

In human communication, non-verbal behaviour such as posture, gesture, gaze, and movement conveys intent, regulates attention, and shapes the emotional tone of exchanges. For social robots and embodied AI agents, this layer remains difficult to design systematically. Current robotic systems often rely on ad hoc motion scripts or isolated gestures that lack consistent semantics, contextual triggers, or social grounding.

This project addresses that gap by building a machine-readable vocabulary of non-verbal behaviours that are both semantically interpretable and robotically executable. It aims to provide a structured foundation for model-driven multimodal interaction where verbal and non-verbal channels are managed coherently within human–AI collaboration frameworks.

### Applications
- Human–Robot Interaction Research – reproducible non-verbal cues for experimental validation.
- Social Robotics Design – building interaction grammars that blend language, gesture, and emotion.
- AI Behaviour Modelling – connecting semantic intent layers to embodied control systems.
- Performance and Theatre Studies – translating human gesture observation into computational embodiment.

### What
The Non-Verbal Behaviour Vocabulary (NBV) is a structured catalogue of human gestures and actions, observed in natural contexts and encoded for robotic execution on the Unitree G1 platform.
Each gesture includes:
- A semantic layer describing its communicative function (e.g., attention directing, de-escalation, approval).
- A context layer detailing the typical social and environmental settings.
- A form and kinematics layer representing the corresponding body posture and motion primitives, linked to executable keyframes for the G1 robot.
- A regulatory layer defining activation conditions and modulation rules that integrate with the [Social Behaviour Regulation (SBR) framework](https://github.com/zhaw-iwi/socialbehaviourregulation_pub).

The resulting vocabulary supports consistent mapping between high-level social intentions and embodied motor actions, enabling reproducible non-verbal behaviour generation for social robotics experiments, user studies, and human–robot interaction design.

### How
The gesture set originates from an [observational study conducted by an actor researcher](https://lachenmithandvordemmund.wordpress.com), who systematically recorded naturally occurring human gestures in everyday public settings such as cafés, stations, markets, and streets. Each observed action was described verbally, contextualised (location, social situation), and annotated with its perceived meaning or communicative intent.

Building on this ethnographic dataset, the gestures were formalised as NBV entries with the following workflow:

#### 1. Semantic encoding
Each gesture was assigned communicative functions and affective cues based on its social interpretation (for example, “Winken – Mir nach!” → summons, group coordination, engaging).

#### 2. Contextual metadata
Tags describe environmental affordances, interaction roles, and proxemics (for example, bahnhof, gruppe, social distance).

#### 3. Form–kinematics mapping
Each gesture was mapped to one or more G1 executable poses (qpos keyframes) corresponding to observed limb configurations.
The resulting JSON structures define reproducible sequences for real-time execution.

#### 4. Integration with SBR and PROMISE frameworks
Coupling rules specify when gestures are triggered, how they align with verbal intentions, and how their amplitude or tempo adapt to social context or emotional regulation.
This enables coordinated multimodal behaviour: speech, gesture, and affect working together as a regulated process.

The repository therefore combines empirical observation, semantic annotation, and embodied implementation into a coherent resource for exploring non-verbal social signalling in human–robot interaction.

### Contents
- `nbv_catalog.json` – catalogue of gestures with names, descriptions, functions, and contexts
- `nbv_coupling_rules.json` – mappings from intents and SBR conditions to gestures with timing and modulation
- `nbv_g1_poses.json` – executable G1 motion definitions for each gesture (XML keyframes)
- `docs/` – background materials and mapping notes from the original ethnographic corpus