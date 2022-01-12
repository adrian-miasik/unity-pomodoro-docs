# Scripting Documentation
## Entry Point
**[PomodoroTimer.cs](../api/AdrianMiasik.PomodoroTimer.yml)**: Our main class / component.
Responsible for controlling the main timer logic, configuring settings, and initializing our related components. 
This class also includes many helper functions such as:
- `Play()`
- `Pause()`
- `Restart()`
- `SwitchState()`
- and many more...See the [class](../api/AdrianMiasik.PomodoroTimer.yml) for a full list of methods.

## [Components](../api/AdrianMiasik.Components.yml)
Components scripts are intended to be used for a **specific purpose**.

| Script/Class Name                                                              | Purpose                                                                                                                                                                                                                                        | High Level Use |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| [AboutPanel.cs](../api/AdrianMiasik.Components.AboutPanel.yml)                 | A theme element page used to display information about our application. Includes a description, social buttons, version number, and a copyright disclaimer.                                                                                    |                |
| [Background.cs](../api/AdrianMiasik.Components.Background.yml)                 | A theme element image used to pull focus off selected elements. The background is our default selection.                                                                                                                                       |                |
| [CompletionLabel.cs](../api/AdrianMiasik.Components.CompletionLabel.yml)       | A theme element used to update the color of the referenced "timer completed" labels.                                                                                                                                                           |                |
| [ConfirmationDialog.cs](../api/AdrianMiasik.Components.ConfirmationDialog.yml) | A theme element associated with a prefab. Used to prompt the user with yes/no questions. Such as confirming their action that can interrupt the active running timer.                                                                          |                |
| [CreditsBubble.cs](../api/AdrianMiasik.Components.CreditsBubble.yml)           | A timed based element used for displaying the author of the app. Intended to minimize itself after a couple seconds with the use of the TimerProgress base class.                                                                              |                |
| [DigitFormat.cs](../api/AdrianMiasik.Components.DigitFormat.yml)               | A theme element that is responsible for generating/creating/managing a digit format which consists of DoubleDigit's and DigitSeparators. This class is also responsible for displaying our timer digits.                                       |                |
| [DigitSeparator.cs](../api/AdrianMiasik.Components.DigitSeparator.yml)         | A class used to update the color of the referenced text component.                                                                                                                                                                             |                |
| [DoubleDigit.cs](../api/AdrianMiasik.Components.DoubleDigit.yml)               | A text field that displays two digits to the user which is intended to be manipulated by our DigitFormat class.. Intended to represent either HOURS, MINUTES, or SECONDS. (See PomodoroTimer.Digits enum)                                      |                |
| [HotkeyDetector.cs](../api/AdrianMiasik.Components.HotkeyDetector.yml)         | Responsible for our detecting and executing our keyboard shortcut actions. Single keys are processed in `ProcessKeys()`, and multi-keys are processed in `ProcessKeybinds()`.                                                                  |                |
| [LabelledDropdown.cs](../api/AdrianMiasik.Components.LabelledDropdown.yml)     |                                                                                                                                                                                                                                                |                |
| [RightButton.cs](../api/AdrianMiasik.Components.RightButton.yml)               | A button used to play/pause the timer. Not a ClickButton since this component relies on the pomodoro timer state and has custom functionality based on the state. Intended to be used in conjunction with a ClickButton core component though. |                |
| [SettingsPanel.cs](../api/AdrianMiasik.Components.SettingsPanel.yml)           |                                                                                                                                                                                                                                                |                |
| [Sidebar.cs](../api/AdrianMiasik.Components.Sidebar.yml)                       |                                                                                                                                                                                                                                                |                |
| [SidebarRow.cs](../api/AdrianMiasik.Components.SidebarRow.yml)                 |                                                                                                                                                                                                                                                |                |
| [SocialButtons.cs](../api/AdrianMiasik.Components.SocialButtons.yml)           |                                                                                                                                                                                                                                                |                |
| [ThemeSlider.cs](../api/AdrianMiasik.Components.ThemeSlider.yml)               |                                                                                                                                                                                                                                                |                |
| [Tomato.cs](../api/AdrianMiasik.Components.Tomato.yml)                         |                                                                                                                                                                                                                                                |                |
| [TomatoCounter.cs](../api/AdrianMiasik.Components.TomatoCounter.yml)           |                                                                                                                                                                                                                                                |                |
| [UPIcon.cs](../api/AdrianMiasik.Components.UPIcon.yml)                         |                                                                                                                                                                                                                                                |                |
| [WriteVersionNumber.cs](../api/AdrianMiasik.Components.WriteVersionNumber.yml) | A script that will write the users current software version to a specific text label.                                                                                                                                                          |                |

### [Core](../api/AdrianMiasik.Components.Core.yml)
Core scripts are intended to be used for a **generic purpose**.

| Script/Class Name     | Purpose                                                                                                                                                                                        | High Level Use                                                                                                         |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| AudioMimic.cs         | A singleton class that allows us to transfer audio from a hidden/destroyed gameobject and play it here instead. Limited to only 1 sound mimic at the moment.                                   |                                                                                                                        |
| BooleanSlider.cs      | A generic toggle in the form of a slider that is used to switch between two states.                                                                                                            | Used for switching the timer from work to break mode. (and vice versa)                                                 |
| BooleanToggle.cs      | A generic toggle in the form of a flip/flop sprite. Supports the following property changes: sprite, tint, and z-rotation. Perfect for 2D use.                                                 | Used on the information button on the top right for switching between timer controls and the information / about page. |
| ClickButton.cs        | A generic button that is used to interact with the software and trigger events based on user input. Supports animations, click hold curves, unity events, and sound FX (with pitch variation). | Used on all of our application buttons.                                                                                |
| ThemeElement.cs       |                                                                                                                                                                                                |                                                                                                                        |
| ThemeElementToggle.cs |                                                                                                                                                                                                |                                                                                                                        |

### Helpers
// TODO

### Wrappers
// TODO

## Interfaces
- **IColorHook.cs**: // TODO
- **ITimerState.cs**: Any class that implement this method will have to define a body method for `StateUpdate()`.  Then anytime the timer changes state such as transitioning from `SETUP` to `RUNNING`, all classes that implement this method will have their `StateUpdate()` method invoked. See enum `PomodoroTimer.States` for context.

## Scriptable Objects
// TODO

## UWP
// TODO

## Editor
Editor scripts are designed for changing the front end of Unity when using their associated core scripts.
- **BooleanToggleEditor.cs**
- **ClickButtonEditor.cs**