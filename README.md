

🧾 **Hand-in-Pocket Detection using MediaPipe**

**Overview**

This project detects human poses in uploaded images using MediaPipe Pose and determines whether a person’s hands are possibly in their pockets.

It performs the following steps:

1. Accepts image upload (via Google Colab).

2. Runs pose estimation using MediaPipe.

3. Draws landmarks and skeleton connections on the image.

4. Analyzes wrist and hip positions relative to shoulder width.

5. Detects whether one or both hands are likely inside pockets.

**Requirements**

Python 3.7+

Google Colab (recommended)

**Dependencies:** OpenCV, MediaPipe, NumPy, Matplotlib

**Workflow**

1. Upload images → The script loads each file into memory.

2. Pose detection → MediaPipe estimates landmarks (wrists, hips, shoulders).

3. Annotation → Landmarks and skeleton are drawn on the uploaded image.

4. Pocket detection logic →

Shoulder width is calculated.

A “pocket zone” is defined around each hip.

If a wrist falls inside the zone → it’s flagged as “hand in pocket.”

**Output**

1. **Annotated Image:** The uploaded photo is displayed with detected pose landmarks.

2. **Text Detection Results:**

"Possible hands in pockets detected."

" - Left hand might be in pocket."

" - Right hand might be in pocket."

"No hands in pockets detected."

**Example Use Cases**

1. Human activity recognition

2. Security monitoring

3. Sports or posture analysis

4. Fashion/retail applications (e.g., style analysis)

**Notes**

1. Works best on full-body images where hips and wrists are visible.

2. May give false positives if hands are near hips but not actually in pockets.

3. Thresholds are relative to shoulder width and may need tuning for specific datasets.
