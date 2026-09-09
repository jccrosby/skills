---
"@jccrosby/skills": patch
---

Fix skill names and display names to match their existing `jccrosby-` folder names.
The skills CLI uses declared names when installing, so folder prefixes alone did not apply.
Existing installations under unprefixed names need removal and reinstallation after this fix reaches GitHub.
