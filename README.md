# Netskope Isolation Management
A Firefox extension that streamlines sending browser traffic through Netskope Remote Browser Isolation. Instead of relying on complex HTTP header management tools, this extension adds a simple `Isolate: true` header to all outgoing requests when enabled, allowing Netskope policies to easily target and isolate traffic.

## Installation

1. **Download** the extension file.
2. Open **Firefox**.
3. Click the **☰ (three horizontal lines)** in the top-right corner.
4. Select **Extensions and themes**.
5. Click the **⚙️ gear icon** → **Install Add-on From File...**.
6. Follow the on-screen prompts to install.

## Netskope Policy Configuration

1. Log in to your **Netskope Administrator Portal**.
2. Navigate to **Policies > HTTP Header**.
3. Click **New HTTP Header Profile**.
4. Remove the default `Host` and `Method` request headers.
5. Click **Add Request Fields**, and choose **Custom**.
6. Enter the following:
   - **Name:** `Isolate`  
   - **Match Type:** `Exact Match`  
   - **Value:** `true`
7. Click **Real-time Protection**.
8. Create a new **Web Access Policy**:
   - **Source:** Add criteria, choose **HTTP Header**, and select the profile you created.
   - **Destination:** Choose **All categories** or specific target categories.
   - **Profile & Action:** Set **Action: Isolate**, and complete remaining fields.
9. **Save and apply** your changes.

## Usage

**Icon Status:** 🟠 Enabled | ⚪️ Disabled  

1. In Firefox, customize your toolbar to **pin the extension** for visibility.  
2. Click the extension icon to **toggle** between **Turn On** and **Turn Off**.  
3. With the extension **enabled** and your **policy configured**, visit a target destination to verify it is isolated.
