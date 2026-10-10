# Advanced Issue — Build the Standup Notification Dot

**Tier:** Advanced · Gates done: 5+
**Track:** Dev (Marketing: amplify when shipped)
**Week:** 3

## The Problem
Challengers visit their office and have no idea
if there are new messages in any room.
No notification. No badge. No signal.

## The Fix
Add a red dot + unread count to each room tab
in the OfficeMessagePanel component.
Use localStorage — no server calls needed.

## Files to Touch
- app/office/[handle]/OfficeClient.tsx
  OfficeMessagePanel component
  Room tab buttons

## How It Works
- On room visit: store timestamp in
  localStorage key: office_last_read_{room}
- On load: count messages after that timestamp
- Show red dot + count if unread > 0
- Clear on room visit

## Definition of Done
- Red dot appears on room tab when new messages exist
- Count shows number of unread messages
- Clears when you open the room
- Works on mobile
- PR opened against ANTCPU/ads intern branch

## AI Assist
Suggested prompt:
"I have a React tab component. Each tab is a chat room.
I want to show an unread message count badge on each tab
using localStorage to track last read timestamp.
Show me the hook and the tab render update."

## Mentor
Arena4 reviews this PR personally.
