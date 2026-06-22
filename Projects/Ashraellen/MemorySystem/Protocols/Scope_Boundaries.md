# Scope Boundaries — MemorySystem

Status: active
Created: 2026-06-22
Updated: 2026-06-22

## Principle

`MemorySystem` is a service layer, not a content archive.

It stores protocols, session logs and memory-routing notes.

It should not store the creative content of books or working literary drafts.

## Current project memory branches

Website memory:

`Projects/Ashraellen/MainSite/`

Grant and institutional memory:

`Projects/Ashraellen/Grants/`

More branches may be added later if needed.

## Books boundary

Do not create book-memory folders inside:

`Projects/Ashraellen/MemorySystem/`

Books, novels and literary projects should remain in their own project folders.

Each concrete book may later have its own local `MemorySystem` inside that book's folder.

Example pattern:

`Projects/Ashraellen/<BookOrCycle>/MemorySystem/`

or, if the book already has a deeper established path:

`Projects/<BookProject>/<Book>/MemorySystem/`

This keeps layers separate:

- global Ashraellen MemorySystem = service memory and routing;
- MainSite = website memory;
- Grants = institutional memory;
- book-local MemorySystem = canon, chapters, characters, versions and creative decisions for that specific book.

The global MemorySystem may reference book-local systems only when coordination requires it.

## Website boundary

Website work belongs to:

`Projects/Ashraellen/MainSite/`

Do not confuse website architecture, public pages and site memory with the internal creative memory of books.

## Grants boundary

Grant strategy belongs to:

`Projects/Ashraellen/Grants/`

MemorySystem only defines how grant chats preserve and update memory.
