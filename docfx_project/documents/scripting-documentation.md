# Scripting Documentation
**For a full list of components, please select a namespace below:**

---

## [Editor](../api/AdrianMiasik.Editor.yml)
Editor scripts are designed for changing the front end of Unity when using their associated core scripts.

--- 

## Components
All scripts intended to be used by our Unity GameObjects reside in this namespace.

### [Base](../api/AdrianMiasik.Components.Base.yml)
Intended to be used as a **base class** or a **generic purpose**. Can be used in more than
one context.

### [Core](../api/AdrianMiasik.Components.Core.yml)
Intended to be used for a **generic purpose**. Can be used in more than one context.

- [Containers](../api/AdrianMiasik.Components.Core.Containers.yml)
  - A generic container intended to **handle a group of [items](../api/AdrianMiasik.Components.Core.Items.yml)**.

- [Helpers](../api/AdrianMiasik.Components.Core.Helpers.yml)
  - A generic set of **tools** / helper scripts.

- [Items](../api/AdrianMiasik.Components.Core.Items.yml)
  - A generic item intended to be **used alone** or **by a [container](../api/AdrianMiasik.Components.Core.Containers.yml)**.
    - [Pages](../api/AdrianMiasik.Components.Core.Items.Pages.yml)
      - Our **content** / contexts. (Only one 'page' is seen at any given moment to the user)

- [Settings](../api/AdrianMiasik.Components.Core.Settings.yml)
  - Scripts related to **saving and loading** user settings / **configurations.**

### [Specific](../api/AdrianMiasik.Components.Specific.yml)
Intended to be used for a **specific purpose**. Used in a single context throughout the
application.

- [Automation](../api/AdrianMiasik.Components.Specific.Automation.yml)
  - Scripts used for **running bulk actions**.
- Platforms
  - Platform specific scripts/data for our target platforms:
    - [Android](../api/AdrianMiasik.Components.Specific.Platforms.Android.yml)
    - [Steam](../api/AdrianMiasik.Components.Specific.Platforms.Steam.yml)
    - [Universal Windows Platform (UWP)](../api/AdrianMiasik.Components.Specific.Platforms.UWP.yml)
- [Settings](../api/AdrianMiasik.Components.Specific.Settings.yml)
  - Interactable **options**. (as seen in the settings page)
  

---

## [Interfaces](../api/AdrianMiasik.Interfaces.yml)
Contracts for scripts.

---

## [Scriptable Objects](../api/AdrianMiasik.ScriptableObjects.yml)
External Settings.

---
