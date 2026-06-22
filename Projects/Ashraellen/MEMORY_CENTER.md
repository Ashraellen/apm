# MEMORY_CENTER — Ashraellen

Status: canonical memory protocol
Updated: 2026-06-22

## Purpose

This file defines the Ashraellen project memory center.

No individual chat should be treated as the permanent memory. The permanent memory lives in the repository.

A chat may act as a memory consultant while it is active, but it must write stable results into `Ashraellen/apm` so future chats can continue from the same state.

## Repository roles

Project memory repository:

`Ashraellen/apm`

Live website repository:

`Ashraellen/ashraellen`

## Main entry file

Start from:

`Projects/Ashraellen/START_HERE.md`

## Current website memory

Website sorted state:

`Projects/Ashraellen/MainSite/SORTED_STATE_2026-06-22.md`

Website master file:

`Projects/Ashraellen/MainSite/MASTER_MainSite.md`

Raw imported website chat memories:

`Projects/Ashraellen/MainSite/Inbox_From_Chats/MS_NN.md`

## Session logs

Every substantial chat should leave a short session log in:

`Projects/Ashraellen/Session_Logs/`

Use numbered files:

`SL_001.md`, `SL_002.md`, `SL_003.md`

## What a session log records

- summary of the work;
- accepted decisions;
- files created or changed;
- paths and URLs;
- commit SHAs;
- open tasks;
- rejected, outdated or uncertain ideas;
- which master files need updating.

## Memory hierarchy

Use this hierarchy:

1. `START_HERE.md` — entry point.
2. Project or area master files — stable canon.
3. Sorted-state files — current working synthesis.
4. Session logs — fresh traces from each chat.
5. Raw imports — old unsorted evidence.

## Rule for future chats

A future chat should first read the entry file and relevant memory files, then work, then record what changed.

The goal is continuity: every chat should become a careful clerk of the project, not a wandering prophet with amnesia.
