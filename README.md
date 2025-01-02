# Unexpected behavior of w-1/2 in flexbox without defined parent width

This repository demonstrates an unexpected behavior of Tailwind CSS's `w-1/2` utility class when used within a flex container that doesn't have a defined width.

The issue is that the child divs only take up half of the *available* width of the parent, which is often not the intended behavior.  This is because flexbox items only expand to their content size unless the parent has a constrained width.  If the parent takes the full width of its container, the `w-1/2` only divides that space in half.

The solution demonstrates how to resolve this by explicitly setting a width on the parent flex container. 