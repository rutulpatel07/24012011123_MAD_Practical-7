# Implementation Plan - Setup Person List

This plan outlines the steps to set up the foundational components for Practical 7: a fixed data model, a refined item layout, and a `RecyclerView` adapter to display person data.

## Proposed Changes

### Data Model & Layout

#### [MODIFY] [Person.kt](file:///E:/Ganpat_College/SEM%20_5/MAD/Mobile_Application_Development_Practicals/24012011123_MAD_Practical7/app/src/main/java/com/example/a24012011123_mad_practical_7/Person.kt)
- Fix typo: `longitide` -> `longitude`.

#### [MODIFY] [single_item.xml](file:///E:/Ganpat_College/SEM%20_5/MAD/Mobile_Application_Development_Practicals/24012011123_MAD_Practical7/app/src/main/res/layout/single_item.xml)
- Change root `layout_height` from `match_parent` to `wrap_content` to prevent each item from taking up the entire screen.

### Adapter & Activity

#### [NEW] [PersonAdapter.kt](file:///E:/Ganpat_College/SEM%20_5/MAD/Mobile_Application_Development_Practicals/24012011123_MAD_Practical7/app/src/main/java/com/example/a24012011123_mad_practical_7/PersonAdapter.kt)
- Implement `RecyclerView.Adapter` to bind `Person` data to `single_item.xml`.

#### [MODIFY] [activity_main.xml](file:///E:/Ganpat_College/SEM%20_5/MAD/Mobile_Application_Development_Practicals/24012011123_MAD_Practical7/app/src/main/res/layout/activity_main.xml)
- Add a `RecyclerView` to the layout.

#### [MODIFY] [MainActivity.kt](file:///E:/Ganpat_College/SEM%20_5/MAD/Mobile_Application_Development_Practicals/24012011123_MAD_Practical7/app/src/main/java/com/example/a24012011123_mad_practical_7/MainActivity.kt)
- Initialize the `RecyclerView` with a sample list of `Person` objects to verify the UI.

## Verification Plan

### Manual Verification
- Deploy the app to a device/emulator.
- Verify that a list of persons is displayed correctly using the `single_item.xml` layout.
- Ensure items don't overlap or take up excess space (root height fix).
