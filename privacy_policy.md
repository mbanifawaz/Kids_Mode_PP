## **Privacy Policy for Kids Mode**

**Last Updated: 27/09/2026**
**App Version: 1.1.2**
**Package: com.mbf.kidsmode**
**Developer: Munes Bani Fawaz (MrGiveItAwayTPK)**

Thank you for using **Kids Mode**. Kids Mode lets a parent hand their phone to a child safely: while Kids Mode is on, the child can only use the apps the parent chose, and leaving Kids Mode needs the parent's PIN, fingerprint or face. This document explains what permissions the app uses, why they are needed, and how your privacy is respected.

Kids Mode is a tool **for parents**. It is set up and controlled by the adult who owns the phone.

---

### **Data Collection and Sharing**

- **No Personal Data Collected**:
   Kids Mode does **not** collect, store or share any personal information about you or your child.

- **No Account, No Ads, No Tracking**:
   There is no sign-in, no advertising and no analytics or tracking of any kind.

- **Nothing Leaves Your Phone**:
   Kids Mode never sends any data to the developer, to a server or to any third party. It does not use the internet to talk to anything outside your phone (see `INTERNET` below for the one local connection it makes).

- **All Data Stored Locally**:
   Everything the app keeps (your settings, the list of allowed apps and app usage times) is stored only on your phone, in the app's private storage. It is deleted when you uninstall the app.

---

### **Permissions and Usage**

Kids Mode only uses a permission for the feature that needs it. Optional features ask for their permission only when you turn them on.

#### **Core Permissions**

1. **Accessibility Service (`BIND_ACCESSIBILITY_SERVICE`, "Kids Mode protection")**
   - **Purpose**: Keeps your child inside the apps you allowed while Kids Mode is on.
   - **Usage**: While Kids Mode is on, the service checks which app and which system windows are on screen. If your child opens an app you did not allow, recent apps, settings, the assistant or the notification bar, it sends them back to the Kids Mode home screen. It also keeps the media volume at or below the limit you set (it watches the volume keys for this), runs the time limit and forced breaks, and measures how long each allowed app is used.
   - **What it does not do**: It does not read, store or send what is on the screen, what is typed, passwords, messages or any other content. It does nothing while Kids Mode is off.
   - Kids Mode shows a clear explanation and asks for your consent inside the app before you turn this service on.

2. **Default Home App (Home role)**
   - **Purpose**: So the Home button or swipe opens the Kids Mode screen while Kids Mode is on.
   - **Usage**: While Kids Mode is off, Home is passed straight to your normal home screen app.

3. **Device Administrator (uninstall protection)**
   - **Purpose**: Stops a child from uninstalling Kids Mode.
   - **Usage**: Kids Mode uses **no** device admin policies (it cannot wipe, lock or change your phone). Being an active admin only blocks uninstalling. You can turn it off at any time in the app (Unlock → "Allow uninstalling Kids Mode").

4. **`USE_BIOMETRIC` / `USE_FINGERPRINT`**
   - **Purpose**: Optional fingerprint / face unlock to leave Kids Mode.
   - **Usage**: Uses Android's own biometric prompt. Kids Mode never sees or stores your fingerprint or face; Android only tells it "success" or "failure".

5. **`READ_PHONE_STATE`**
   - **Purpose**: So you can answer phone calls while Kids Mode is on.
   - **Usage**: Kids Mode only notices when a call is ringing or in progress, then brings your phone app's call screen to the front. It does not read phone numbers, contacts or call history.

6. **`KILL_BACKGROUND_PROCESSES`**
   - **Purpose**: Closes the app your child was using when a forced break starts or the time limit runs out.

7. **`POST_NOTIFICATIONS`**
   - **Purpose**: Shows the notification used to type the Wireless debugging pairing code during setup, and the notification Android requires while the optional camera distance check is running.

#### **Optional: Full Lock (Wireless Debugging)**

8. **`INTERNET`, `ACCESS_NETWORK_STATE`, `ACCESS_WIFI_STATE`, `CHANGE_WIFI_MULTICAST_STATE`, `WRITE_SECURE_SETTINGS`**
   - **Purpose**: The optional **full lock** switches off the notification bar, quick settings, recent apps and power-button shortcuts at system level.
   - **Usage**: If you choose it and pair it once (Settings → Developer options → Wireless debugging → Pair device with pairing code), Kids Mode connects to your **own phone's** Wireless debugging over Wi-Fi. This connection stays **inside your phone**: it is used only to run the system commands the full lock needs (such as switching the notification bar off and back on, and giving Kids Mode the `WRITE_SECURE_SETTINGS` and phone permissions it needs). `WRITE_SECURE_SETTINGS` is used only to switch Wireless debugging and Kids Mode's own protection service back on, for example after a restart.
   - Kids Mode saves your original power-button settings before changing them and restores them when Kids Mode ends.
   - You can skip the full lock; Kids Mode then works without it.

#### **Optional: Too-Close Warning (Eye Comfort)**

9. **Proximity sensor**
   - **Purpose**: Covers the screen with a dim reminder when the phone is held too close to the child's face.
   - **Usage**: Reads only "near" or "far" from the sensor. No permission is needed and nothing is stored.

10. **`CAMERA`, `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_CAMERA`**
    - **Purpose**: On phones whose proximity sensor can't be used for this, you can choose the front camera instead.
    - **Usage**: While Kids Mode is on, the front camera is checked a few times per second **on the phone** (Google ML Kit face detection, running entirely on the device) to measure how big a face looks, and so how close it is. **No photos or video are saved, shown or sent anywhere**, and no face is recognised or identified; only the size of a face in the picture is used. Android shows its green camera indicator while this runs. It is off unless you turn it on, and it stops when Kids Mode ends.

---

### **Data We Store Locally**

All of this stays in the app's private storage on your phone:

- Your settings: allowed apps, time limit, breaks, volume limit, eye comfort, theme and language
- Your **parent PIN**, stored only as a **one-way salted hash** (the PIN itself is never stored)
- **App usage times** in Kids Mode (per app, per day, the last 14 days), shown only in the app's Activity page
- The Wireless debugging pairing key (created by the app, used only to connect to your own phone)
- Your original power-button settings, kept only until Kids Mode restores them

Uninstalling Kids Mode deletes all of it.

---

### **Third-Party Services**

- **Google ML Kit (on-device face detection)**: used only for the optional camera too-close warning. It runs on your phone. Kids Mode sends no images to Google or anyone else, and ML Kit's usage-statistics uploader is switched off in the app, so ML Kit sends nothing either.
- **libadb-android (open source)**: used only for the optional full lock, to talk to your own phone's Wireless debugging. It makes no connection outside your phone.

Kids Mode contains no advertising or analytics SDKs.

---

### **Features and Privacy**

#### **1. Allowed Apps**
Only the apps you choose appear on the Kids Mode screen. Links that open other apps (browser, store, share sheet) are blocked.

#### **2. Time Limit and Forced Breaks**
Worked out on your phone. When a break starts, the open app is closed and a break timer shows.

#### **3. Maximum Volume**
Media volume cannot go above the limit you set.

#### **4. Eye Comfort**
Optional warm screen filter and too-close warning (see above).

#### **5. Phone Calls**
Calls can be answered and ended in Kids Mode; notifications from other apps stay hidden.

#### **6. Activity**
Shows how long each allowed app was used, only on this phone.

#### **7. Languages**
English and Arabic.

---

### **Your Privacy Rights**

- **Access**: Everything Kids Mode keeps is visible in the app
- **Deletion**: Uninstall the app to delete all local data (turn off uninstall protection first: Unlock → "Allow uninstalling Kids Mode")
- **Control**: Every permission can be turned off in Android Settings; optional features can be turned off in the app
- **Portability**: No data is stored on external servers, so there is nothing to export

---

### **Children's Privacy**

Kids Mode is used by parents to supervise their own children on their own phone. It does **not** collect, store or share any personal information from children. The only information about a child's use is the app usage time per day, which stays on the phone and is shown only to the parent in the app. The optional camera check measures face size on the phone and never saves or sends images.

---

### **Changes to This Privacy Policy**

We may update this Privacy Policy from time to time to reflect changes in app features or legal requirements. Any changes will be reflected in this document with an updated "Last Updated" date.

**Version History:**
- **1.1.2** (27/09/2026): Initial published version. ML Kit's usage-statistics uploader is switched off, so nothing at all leaves the phone.

---

### **Ownership and Developer Rights**

**Kids Mode** is developed and owned by **Munes Bani Fawaz** (MrGiveItAwayTPK). All rights, including the app's design, source code and intellectual property, belong to the developer.

---

### **Contact Information**

If you have any questions, concerns or requests regarding this Privacy Policy or your data, please contact:

- **Developer**: Munes Bani Fawaz (MrGiveItAwayTPK)
- **Email**: m.banifawaz@outlook.com

---

### **Acceptance**

By using **Kids Mode**, you acknowledge that you have read and understood this Privacy Policy.
