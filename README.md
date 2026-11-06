# OMNI Keypad Designer

OMNI Keypad Designer is a Windows desktop app for designing button images for
Harman BSS OMNI dynamic keypads and deploying them to the keypad over your
network. Each button gets an Off and an On image, and optionally an ALT image.
You build each image from a background, your own image, an icon, and text.

The designer runs on your computer. You don't need internet access to design
buttons or deploy them.

## Supported keypads

The designer supports these OMNI keypads, running firmware 1.1.x:

| Model | Tabletop version | Buttons | Dial and LED ring |
|---|---|---|---|
| OMNI-KP-6B | OMNI-KP-T6B | 6 | No |
| OMNI-KP-6BV | OMNI-KP-T6BV | 6 | Yes |
| OMNI-KP-8BV | OMNI-KP-T8BV | 8 | Yes |
| OMNI-KP-V | None | None | Yes |

Keypad deployment is experimental. Before you deploy to a keypad on a live
system, see [Before you deploy](#before-you-deploy).

## Install the designer

To install the designer, you need Windows 10 or Windows 11. You don't need to
install Python or anything else first.

1. Go to the [latest release](https://github.com/Madison-AV/omni_keypad_designer-releases/releases/latest).
1. Under **Assets**, download `OMNI_Keypad_Designer_<version>.zip`.
1. Extract the zip. It contains the installer and the release notes.
1. Run `omni_keypad_designer_setup_<version>.exe`.
1. Read the Madison Software Licence, and accept it to continue.
1. Choose whether to install for everyone on the computer, which needs admin
   rights, or just for you.

The installer adds **OMNI Keypad Designer** to the Start menu. To update to a
new version, run the new installer. Your projects stay where they are.

To uninstall the designer, go to **Settings > Apps > Installed apps**, find
**OMNI Keypad Designer**, and click **Uninstall**.

## Get started

1. Open **OMNI Keypad Designer** from the Start menu.
1. To start a project, click **File > New Project**, and choose a name and
   keypad model. To work on a keypad's current design instead, enter its IP
   address, or click **Scan**, and then click **Import**.
1. Click a button on the keypad view, then click a state (Off, On, or ALT) to
   edit it. Turn parts on with their switches, and click a part to change it.
1. To save, click **File > Save** or press Ctrl+S.
1. To put the project on a keypad, enter its IP address and click
   **Deploy**. The keypad restarts with the new design in about 20 seconds.

For the full guide, click **Help > User Guide** or press F1 in the app.

The designer keeps your projects, keypad backups, and button library in
`Documents\OMNI Keypad Designer`. To open that folder, click **File > Open
Data Folder**.

## Before you deploy

Deploying replaces the keypad's whole design. Each deploy first backs up the
design that was running, and if the deploy fails, the designer offers to
restore it. To see or restore backups, click **Keypad > Backups**.

This release is pre-release software. As the licence says, a deployment can
leave a keypad needing a reset or firmware recovery. Test on a keypad that
isn't in service before you deploy to a live system.

## Get help

To report a problem or ask a question, email
[support@madisonav.com.au](mailto:support@madisonav.com.au). To help us
troubleshoot, include:

- The app version, from **Help > About**.
- The keypad model and its firmware version.
- What you did, what you expected, and what happened instead, including the
  full text of any error message.
