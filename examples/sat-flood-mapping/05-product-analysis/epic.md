# Epic: Product analysis (Sat-Flood-Mapping)

Does the *system* produce trustworthy flood maps on new inputs? Test on recent Sentinel-2 acquisitions from real events (not in Sen1Floods11), stress the pipeline with edge cases, and hand it off to someone outside the team.

The realistic-input test here is unusually powerful because **recent flood events keep happening**. You can grab a Sentinel-2 tile from a flood event that occurred *after* Sen1Floods11 was published — that's a genuine "out-of-distribution" test the model has never seen.

## Cards in this epic

1. End-to-end tests on real recent floods
2. Integration and edge-case tests
3. Hand-off test — someone else runs it
