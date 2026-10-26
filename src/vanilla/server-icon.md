# Server icon {#server-icon}
The icon must meet the following requirements:

- size of 64x64 pixels
- file name *server-icon*
- format (and extension) *png*

For a rectangular source image, crop a square around the part you want to keep before resizing it to 64x64 pixels. This avoids stretching the image. Export it as PNG, then save it as *server-icon.png*.

An image editor can do these steps. For a browser option, the [ServerBuddy icon maker](https://serverbuddy.net/tools/minecraft-server-icon-maker) crops from the center and exports a 64x64 PNG named *server-icon.png*. Check the preview because the center crop can remove details near the edges.

Thus, the resulting icon must be a 64x64 px *server-icon.png* file. If the icon does not meet one of the requirements, the icon will not appear in the server list.

Upload the prepared file to the server root, alongside *server.properties*. If a proxy provides the icon, use the proxy's directory instead, as explained below.

**After the icon is uploaded, the server must be restarted for the changes to take effect.**

## Icon not working {#server-icon-doesnt-work}
The icon does not display correctly in the following cases:

- The icon does not meet the above requirements

Make sure the icon meets all of the above requirements, including that the resulting file is not named *server-icon.png.png* (due to disabled file extensions on the *Windows*, see [here](../other/desktop.md#file-extensions)).

- Cache

The client may have information about the old/non-functional icon temporarily cached. In this case, the icon will be displayed correctly on <https://mcsrvstat.us/>, but not in the client. If you see the icon correctly on <https://mcsrvstat.us/> but not in the client, you usually just need to restart the client.

- The file is not valid *PNG*

If you originally had the icon in a different format, such as *JPEG*, and you "converted" the icon to *PNG* by overwriting the extension, the icon is not a valid *PNG* file. To convert another format to *PNG*, you need to use a converter (there are many online converters available on the internet).

- Plugin

Some plugins can affect the icon settings, and thus the vanilla icon will not work (usually [MOTD](motd.md#motd) plugins have this feature, which should be disableable in the plugin configuration).

- Uploading icon on backend server when running a proxy

If you run a proxy, the icon must be uploaded on the proxy server, not some of the [backend](~backend-server) ones.

<!-- bit depth over 32 bits - have to verify --->
