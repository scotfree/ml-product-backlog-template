# Replace stubs with real components (incremental)

Swap one stub at a time. The pipeline stays runnable at every step. Order: (1) real IQA gate → (2) real detector → (3) real pose lookup → (4) real camera (last, requires the Pi hardware and Embedded's `cv2.VideoCapture` wrapper).

- **Upstream/downstream:** Each swap has its own upstream: IQA is self-owned; detector consumes Modeling epic's checkpoint; pose lookup depends on Data A's API being live on the Pi; real camera depends on Embedded's Pi image having the camera wired up.
- **Definition of done:** Real component passes the same interface tests as the stub it replaced. `pytest tests/` still green after each swap.
- **Demo:** For each swap, show pipeline running with the new real stage; contrast a published message pre- and post-swap.
- **Subtasks:**
  - One card per stub-to-real swap, filed in the sprint that swap lands in.
