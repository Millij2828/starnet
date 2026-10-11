# EVO visual testing prototype

Open `frontend/evo-visual-testing.html` in a browser. This standalone prototype is separate from the Starnet application and does not call its runtime, providers or tools. No real AI execution or persistent results are claimed.

Included: four shaped rooms, four agents, portal travel, graduation gate, role abilities, walking/running, crew dashboard, fullscreen fallback and group mission presets.

Reviewed fixes:
- Separate mission summary from command validation feedback.
- Reject ambiguous multi-preset instructions without discarding the draft.
- Explicit queued work can complete prerequisite training with autonomous routine selection off.
- Cancel unfinished mission assignments without counting them as successful.
- Preserve the submitted brief on assigned tasks for agent status questions.
- Avoid duplicate completion messages and claims that experiment logs were persisted.

Validation: executed JavaScript against a mocked DOM and real Canvas renderer; verified crew selection, pause, chat, expanded fallback, ability completion, faster movement, full group briefing completion, ambiguous prompt handling, and queued mission cancellation. This is not a full browser/end-to-end test or a Starnet test-suite run. Browser fullscreen and responsive layout require manual verification. Save/resume, agent-to-agent collision avoidance, real tool permissions and runtime event integration remain future work.

Architecture references: shared/events.js, frontend/app/worldmodel.js, frontend/app/taskconversation.js, frontend/app/warroom.js. Keep EVO artwork and name separate from Starnet branding.
