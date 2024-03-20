# ucExplorerTree
ActiveX Control Wrapper for INamespaceTreeControl

Version 1.0.1 - Released 20 Mar 2024

This is a UserControl/ActiveX control that, like ucExplorerBrowse and IExplorerBrowse, wraps the Windows shell component [INamespaceTreeControl](https://learn.microsoft.com/en-us/windows/win32/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol), the object that makes up an Explorer window's left pane.

![image](https://github.com/fafalone/ucExplorerTree/assets/7834493/c1a804ca-956e-4642-b0f7-9db4adec653c)

The control is set up to look as similar to Explorer as possible with the default options; indeed I got a reference to one in an Explorer window and queried the flags it had. There's some differences; it's not truly the same object. For instance querying the roots doesn't show all the root items you actually see. I've added Libraries and Network back in; along with QuickAccess they're optional. You can also substitute ThisPC for Desktop, or insert the root nodes yourself by specifying a path.

Requires twinBASIC Beta 472 or newer to run the demo or build the OCX. Windows Vista or newer is also required. Common Controls 6.0 must be enabled by manifest.

But after that, this was built with the idea it should be creatable in other standard COM hosts. A fairly simple control to test tB's ability to make controls with wide compatibility.

IMPORTANT: Not all options work on all Windows versions, and some only work if set at startup (i.e. whatever they're set to in the Form designer). Some notable issues on Windows 10 include it seems to not produce double-click or right-click notifications, won't cycle through additional check states beyond checked/unchecked, and the items for which extra buttons Delete and Refresh are applied make no sense.

If you want more features and control, check out my [ucShellTree control](https://github.com/fafalone/ShellControls), which implements a namespace tree like this from scratch.

Binary releases will be coming soon after I test them. Right now this has only been tested as a UserControl inside twinBASIC.
