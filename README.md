# ActionScript 3 Event Listener Leak Bug Report

This repository demonstrates a common ActionScript 3 bug related to event listener leaks.  When dynamically adding MovieClips to the display list and attaching event listeners, removing the MovieClip without removing the listeners can lead to unexpected behavior or runtime errors. The `bug.as` file shows the problematic code, and `bugSolution.as` provides the corrected version.

## Problem

The issue occurs because event listeners remain active even after the target object (MovieClip) is removed from the display list. This can result in errors or unexpected behavior, especially when the removed object is referenced again later.  This is a memory leak, and in larger applications can lead to performance issues and crashes.