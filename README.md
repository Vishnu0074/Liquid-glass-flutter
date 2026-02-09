Custom Glassmorphism SnackBar for Flutter

A reusable glass-style floating SnackBar with blur effect, gradient tint, and error/success states.
Designed to look modern, responsive, and consistent across phones and tablets.

Features

Glassmorphism blur background using BackdropFilter

Gradient tint for success and error states

Floating SnackBar style

Tablet-friendly max width handling

Reusable static helper method

Minimal setup — just call one function

Installation

Copy the file into your Flutter project:

lib/utils/custom_snackbar.dart

Then import it wherever needed:

import 'package:your_project/utils/custom_snackbar.dart';

Basic Usage

Show success snackbar:

CustomSnackBar.show(
context,
message: "Saved successfully!",
);

Show error snackbar:

CustomSnackBar.show(
context,
message: "Something went wrong",
isError: true,
);

Custom duration example:

CustomSnackBar.show(
context,
message: "Processing complete",
duration: Duration(seconds: 5),
);

Behavior Overview

message → Text displayed inside snackbar
isError → Switches color and icon to error style
duration → How long snackbar stays visible

Default duration: 3 seconds

Responsive Design

Phone: full width with margins
Tablet: constrained width (about 520px) centered

This prevents overly stretched snackbars on larger screens.

Requirements

A Scaffold must exist in the widget tree

BuildContext should belong to a visible screen

Flutter SDK must support BackdropFilter (standard Flutter)

Customization Ideas

You can tweak:

Blur intensity (sigmaX, sigmaY)

Tint colors

Border radius

Icons

Gradient opacity

Example tint colors used:

Success tint: Color(0xFF007873)
Error tint: Color(0xFFB3261E)

Recommended Usage

Good for:

API success or failure messages

Form validation feedback

Notifications

Quick status updates

License

Free to use in personal or commercial Flutter projects.
