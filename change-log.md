# Changelog

<!--
This file lives at change-log.md in the liquid-life-singular repo.

Instructions for appending a new entry (future sessions read this):
1. Find or create the section for the current work week: "## Week of <Mon>–<Fri>, <Year>"
   Weeks run Monday through Friday only — weekends are excluded from the range (a change made
   on a Saturday/Sunday still gets folded into that same Mon–Fri section, it just doesn't
   extend the displayed date range).
2. Add one bullet per client-visible change, plain language, no file paths or internal IDs.
3. Do NOT add repo-organization, refactor-only, or internal-naming changes — see the
   github-changelog skill's client-facing rules (exclude internal architecture, field/table
   IDs, debugging narrative; include only what a client would notice or asked for).
4. Log the FINAL shipped state of a feature once it's done, not each mid-build iteration.
   If a feature gets reworked multiple times in one session before the user is happy with it
   (e.g. a chip's color/shape/sizing tweaked three times, a toggle changed from a slider to a
   dropdown), write ONE bullet describing how it ended up, not one bullet per attempt. Never
   add a bullet for a change that got superseded or reverted later in the same session — only
   the client-visible end state belongs here. When updating an entry that's still mid-session
   (not yet a settled feature), it's fine to edit/replace the existing bullet in place instead
   of appending a new one.
5. Newest week goes at the top, directly under the title.
-->

## Week of Aug 31–Sep 4, 2026

- Fixed a Direct Mail Tracker bug where a campaign sent to more than one audience only counted the parcels from one of them toward its actual recipient count — the campaign's real reach was being undercounted. Every linked audience is now combined correctly (with shared parcels only counted once), and the fix has been applied retroactively to every existing campaign, so recipient counts across the board are now accurate.

## Week of Aug 24–28, 2026

- On the main Tasks page, you can now mark a task complete right from its row — click the status chip and pick a new status, no need to open the task first. The Status column now appears first in the table, and marking a task Done smoothly slides the rows below it up instead of jumping. You can also press Ctrl+Z (Cmd+Z on Mac) to undo your last status change.
- Every color-coded label across Tasks, Deals, and Contacts — status, priority, call outcome, and unit contract status — now matches the exact color and solid-fill pill style set up for that value in Airtable, everywhere it appears, sized to its own text.
- The Tasks page now has a List/Kanban toggle (a dropdown, defaulting to List, at the right of the toolbar, with a quick smooth transition between the two). The List view adds a matching Due Status column and filter. In Kanban, a "Group by" dropdown splits columns by Due Status (Overdue/Today/Upcoming) or by Status — grouped by Status, you can drag a task card between columns to change its status. Kanban columns no longer grow taller than your screen: each column scrolls its own cards (up to 20 at a time) and switches to Prev/Next paging beyond that.
- You can now sort tasks on the Tasks page: click a column header in List view to sort by it (click again to reverse the order), or use the "Sort by" box next to the search bar in Kanban view. Sorting carries over when you switch between List and Kanban.
- Fixed an issue where a campaign sent to more than one audience only ever showed one of them, everywhere you looked at it. Now every audience it was sent to shows up correctly. A campaign's page also now shows all of its audiences in a clean, easy-to-read list instead of getting cluttered when there are many. Picking audiences when creating a campaign is easier too — your choices are highlighted and move to the top of the list, and show up as a short, tidy summary instead of taking over the screen.

## Week of Aug 10–14, 2026

- Fixed an issue in the Direct Mail Tracker where creating a new audience and filtering for "Houses" returned no results, even though the same filter worked fine in the data view. Audiences can now be filtered by property type correctly.
- New Deal now defaults the Deal Owner to whoever is creating it, instead of always defaulting to Albert Miles.
- Who can be selected as a Deal Owner is now easy to manage — add or remove someone from the list without a code change.
- You can now delete a campaign from the Direct Mail Tracker, with a confirmation warning if it has deals linked to it.
- The Campaign picker on a Deal now finds a campaign by its mailed date typed any way you'd naturally write it (e.g. "7/10", "july 2026", "jul 10"), not just an exact match on how the date is displayed.
- Contacts now have an optional "Preferred Name" field, separate from the legal name — available on the contact's detail page and on the New Lead intake form.
- Tasks now show soonest-due-first, consistently, in a deal card's quick-preview popup and in the Contact detail page — previously unsorted in both places.
- Show the mailed date next to each campaign option in the dropdown.

## Week of Aug 3–7, 2026

- Each Campaign option now shows its mailed date on the right, sorted newest to oldest instead of alphabetically.
- In Log a Call, Call Type is now optional — only Outcome is required.

## Week of Jul 27–31, 2026

- Fixed a clipboard copy error that could happen when copying contact info from within Airtable.
- Task Tracker rows now show contact info (with one-click copy buttons) and a clickable link to the linked deal.
- Contacts now show the real date and time a contact came in, instead of the date the bulk import ran — visible in the Contacts list, on the Contact detail page, and on the linked Deal's detail page.
- Dates and times across the CRM now include the timezone.
- You can now click a contact from within a deal to open that contact's full detail page directly, without leaving the deal.
- The contact submission form's notes field is now labeled "Additional Information," and you can add your own private "Internal Notes" on a contact, separate from what came in on the form.
- You can now delete a deal, from either the deal popup or the full deal page, with a confirmation warning before it's removed.
- Contact, deal, and team-member search results and pickers are now sorted alphabetically.
- Fixed the Kanban card's "Next task" indicator sometimes showing an outdated task instead of the soonest upcoming one. Task Tracker rows are now sorted newest to oldest.
- You can now edit a deal's Close Date and Signed Rental Date directly from the Kanban card, without opening the full record.
- The Contacts list "Created" column header is now clickable to sort newest/oldest; the Deal Kanban board has a new toolbar toggle to sort each column by Est. Close Date.
- Deleting a contact is now much faster to see reflected in the list, while still giving you a few seconds to undo before it's gone for good.
- Removed the "Direction" field from the Log a Call form — it's no longer asked for when logging a call.
- Contacts and deals now show a Units section (below Deals on the Contact page, after Contacts on the Deal page) listing any unit tied to their linked deals, with a detail view for Unit Code, Parcel Unit, Complex, and Contract Status.
- A Unit can now be linked to more than one deal — the Unit picker on the Deal page no longer hides units already assigned elsewhere.
- The Deal popup now also shows the Units section, matching the full deal page.

## Week of Jul 20–24, 2026

- Deal popup now requires a Close Lost reason and shows the Closed Won checklist, matching the full deal page.
- A deal's Unit field now locks or unlocks automatically based on whether a Parcel is linked and a matching unit exists; the "Create Unit" button disappears once a unit is linked.
- Fixed older deals getting permanently stuck with a locked Unit field.
- Unit search now explains when nothing matches and offers to fix the search or create a new unit.
- Deals search now shows a dropdown of matching results instead of filtering the whole board.
- Task detail no longer allows changing which deal a task is linked to.
- Added CSV/PDF export for an audience's contact list in the Direct Mail Tracker.
- Added a Unit Information popup, and contact email/phone can now be copied with one click.

## Week of Jul 13–17, 2026

- Opening a deal from Contacts now shows the full deal page instead of a small popup.
- Added a "next task" indicator on deals, drag-and-drop on the Kanban board, a reason field for Closed Lost deals, a filter by contact type, inline task editing, and the ability to log a call directly on a deal.
- Contact detail page now includes a Tasks section, a Call Log section, and shows Contact Type.
- Tasks created from a call are now marked with an icon, can be filtered, and link back to the original call.
- Task detail's "Open Contact" and "Open Deal" links are now fully functional.
- Deal name is now editable directly from its popup or full page.
- Added a "+ New Deal" button to a Contact's Deals section, so you can create a deal without leaving the contact.
- Date fields now open a calendar picker when clicked, instead of requiring manual typing.
- Deal/Contact pickers in Tasks are now searchable.
- Parcels can now be searched by Unit Code.
- Campaign and Close Lost Reason options now reflect what's actually configured instead of a fixed list; fixed a gap where Contacts handled Close Lost differently than Deals.
- Deal and Contact popups widened for readability; added a shortcut to open the full Kanban page; fixed a date-rollover bug and a layering bug where deal/contact views could render behind each other.

## Week of Jul 6–10, 2026

- Contact info fields are now editable directly, saving automatically as you type.
- Fixed a bug where due dates weren't displaying correctly in Tasks, and a bug that could fail to save a contact's name.
- Fixed an issue where some task updates were failing silently with no error shown.
- Clicking a linked Contact or Deal now opens a quick view in place, instead of navigating away from what you were doing.
- Fixed a layout bug where nested Contact/Deal views could render behind each other; standardized the "create task" form.
- Clearer status descriptions and warning messages when a Contact or Deal is missing.
- Added the ability to delete a Contact, with an undo option (with a grace period so you don't lose it by accident); acquisition-only records are now hidden from the main views.
- Task creation from a Deal now shows a clear error message if something goes wrong, instead of failing silently.
