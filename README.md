

🧾 **# Hand-in-Pocket Detection using MediaPipe**

**Overview**

This project detects human poses in uploaded images using MediaPipe Pose and determines whether a person’s hands are possibly in their pockets.

It performs the following steps:

Accepts image upload (via Google Colab).

Runs pose estimation using MediaPipe.

Draws landmarks and skeleton connections on the image.

Analyzes wrist and hip positions relative to shoulder width.

Detects whether one or both hands are likely inside pockets.

**Requirements**

Python 3.7+

Google Colab (recommended)

**Dependencies:** OpenCV, MediaPipe, NumPy, Matplotlib

**# Workflow**

Upload images → The script loads each file into memory.

Pose detection → MediaPipe estimates landmarks (wrists, hips, shoulders).

Annotation → Landmarks and skeleton are drawn on the uploaded image.

Pocket detection logic →

Shoulder width is calculated.

A “pocket zone” is defined around each hip.

If a wrist falls inside the zone → it’s flagged as “hand in pocket.”

**# Output**

Annotated Image: The uploaded photo is displayed with detected pose landmarks.

Text Detection Results:

"Possible hands in pockets detected."

" - Left hand might be in pocket."

" - Right hand might be in pocket."

"No hands in pockets detected."

**# Example Use Cases**

Human activity recognition

Security monitoring

Sports or posture analysis

Fashion/retail applications (e.g., style analysis)

**# Notes**

Works best on full-body images where hips and wrists are visible.

May give false positives if hands are near hips but not actually in pockets.

Thresholds are relative to shoulder width and may need tuning for specific datasets.
