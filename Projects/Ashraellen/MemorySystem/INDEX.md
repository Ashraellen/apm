# MemorySystem — Ashraellen

Status: canonical memory system
Created: 2026-06-22

## Purpose

`MemorySystem` is the service layer for Ashraellen project memory.

It keeps the project from being scattered across separate chats.

Individual chats may work locally, but stable memory is stored in GitHub.

## Core idea

The repository is the long-term memory.

Chats are working rooms.

Each substantial chat must read the relevant memory before work and record what changed after work.

## Main files

Memory center protocol:

`Projects/Ashraellen/MemorySystem/MEMORY_CENTER.md`

New chat workflow:

`Projects/Ashraellen/MemorySystem/Protocols/New_Chat_Workflow.md`

Website memory workflow:

`Projects/Ashraellen/MemorySystem/Protocols/Website_Memory_Workflow.md`

Session logs:

`Projects/Ashraellen/MemorySystem/Session_Logs/`

Templates:

`Projects/Ashraellen/MemorySystem/Templates/`

## Project repositories

Project memory:

`Ashraellen/apm`

Live website:

`Ashraellen/ashraellen`

## Website memory branch

Main website memory lives in:

`Projects/Ashraellen/MainSite/`

Current sorted website state:

`Projects/Ashraellen/MainSite/SORTED_STATE_2026-06-22.md`

Website master file:

`Projects/Ashraellen/MainSite/MASTER_MainSite.md`

Raw imported website chat memories:

`Projects/Ashraellen/MainSite/Inbox_From_Chats/MS_NN.md`

## Rule

If a chat changes the project, it must leave a memory trace.

If a chat only answers a small question and changes nothing, a session log is not required.
