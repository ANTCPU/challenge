# Advanced Issue — Wire Reply Threading in Office Messages

**Tier:** Advanced · Gates done: 5+
**Track:** Dev (Marketing: amplify when shipped)
**Week:** 3

## The Problem
Office messages have no threading.
The standups room has a Day 10 question posted.
Challengers cannot reply to it — only post new messages.
Threading would make standups scannable in one view.

## The Fix
Add reply_to_id to office_messages table.
Update the OfficeClient.tsx message panel to show replies indented.

## Files to Touch
- Supabase: ALTER TABLE office_messages ADD COLUMN reply_to_id uuid
- app/office/[handle]/OfficeClient.tsx — OfficeMessagePanel component
- app/api/internship/office/route.ts — include reply_to_id in SELECT

## Definition of Done
- reply_to_id column exists in DB
- Messages with reply_to_id render indented under parent
- Standup question shows replies threaded below it
- PR opened against ANTCPU/ads intern branch

## AI Assist
Suggested prompt for Cursor:
"I need to add reply threading to a Next.js chat component.
The messages table has id, content, author_name, created_at.
I want to add reply_to_id. Show me the SQL migration and
the React component change to render replies indented."

## Marketing Observer Brief
When your dev partner opens this PR — share it everywhere.
"The antcpu virtual office just got threading. Here is the PR."
Link the PR. Link their office page. Screenshot the before/after.
This is a real feature shipping to a live product.

## Mentor
Arena4 reviews this PR personally.
