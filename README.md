BioSim

A browser-based simulator for planning and testing FTC autonomous routines. Build an auto from steps or draw a path on the field, watch the robot run it, and export Java for your LinearOpMode.

Everything lives in one file, index.html. There is nothing to install and no server to run.

Run it
Online: open the GitHub Pages link for this repo (Settings → Pages shows it).
Locally: download index.html and open it in any modern browser.
Hosting on GitHub Pages
Put index.html in the root of a public repo.
Go to Settings → Pages.
Set Source to Deploy from a branch, choose main and / (root), then click Save.
After a minute or two the site is live at https://YOURNAME.github.io/REPO-NAME/.

To update, upload a new index.html with the same name and commit it.

What it does
Field: the official BIOBUZZ field image, 144″ square. Red alliance is at the bottom, blue at the top.
Drive types: tank (two motors) or strafer (mecanum). Switch with the toggle.
Steps: Drive, Turn, Timed power, Wait, Shoot, plus Strafe and Move in strafer mode. Steps are collapsible.
Draw a path: use the draw tool and the robot follows your line. Smoothing straightens small wobbles. In strafer mode, "keep heading" holds the robot's facing. Drawn paths can be erased or undone.
Starting position: use Set start to click or drag the start pose, or type X, Y and heading. The Turn robot buttons rotate the start heading. "Snap start to the wall" keeps the robot touching the wall, and a check tells you if the start is illegal.
Hive: the robot can drive under the hive by default. Untick the box to make it solid. Flowers and walls always block the robot.
Shoot: each step has Balls, Power and Seconds. The robot stands still and the sim shows balls flying out. It does not aim or score.
Match your robot: a calibration card adjusts top speed, track width and wheel diameter from real tests.
Motors: set each motor's name, port and whether it is reversed, including the shooter motor.
Java export: generates an Autonomous LinearOpMode.
Time-based by default.
Optional IMU turns for accurate angles. Choose your hub logo and USB direction.
Optional encoder driving. Enter your counts per wheel turn and wheel diameter.
The shooter motor is only included when the auto has a shoot step.
Save and share: your auto is saved in your browser automatically. Use export and import to move autos between people or devices.
Themes: dark by default, with a light theme button.
Coordinates
The origin is the centre of the field. +X is toward the audience, +Y is toward the blue side.
Heading 0° faces +X. Positive turns are counter-clockwise (left).
Default start is (0, −63) facing 90°, touching the red wall.
Limits
The AI prompt box only works inside claude.ai. It uses the viewer's own Claude account and does nothing on GitHub Pages. Everything else works anywhere.
It is a simulation. Real robots drift, so tune the generated Java on the real field. Use the calibration card and the IMU and encoder options to get closer.
Saved autos stay in each person's own browser. They are not shared between users unless exported.
The shoot step only takes time. It does not model ball flight or scoring.
Using the exported Java
Copy the code into a new OpMode in your FTC project.
Check that the motor names match your robot's configuration.
Test on your own robot and adjust powers and times.
Credits

Built for FTC team 23964 MSM.
