<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/Default.aspx) (VB: [Default.aspx](./VB/Default.aspx))
* [Default.aspx.cs](./CS/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/Default.aspx.vb))
<!-- default file list end -->
# ASPxGridView - How to update an external control during a callback
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e2379/)**
<!-- run online end -->


<p>By default, the ASPxGridView works during callbacks and there's no way to update an external control (that isn't a child control of the callback owner) on the server side. The following article describes this limitation in detail:</p><p><a href="https://www.devexpress.com/Support/Center/p/K18387">The Concept of Callbacks</a></p><p>However, the ASPxGridView as any other ASP.NET control has the <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxGridViewASPxGridView_JSPropertiestopic">JSProperties</a> feature that allows passing a value from the  server to the client. Also, the client-side EndCallback is raised each time when a callback is executed successfully.<br />
So, it is possible to set a JSProperty on the server, get it on the <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxGridViewScriptsASPxClientGridView_EndCallbacktopic">EndCallback</a> and change a "target" control using its client-side capabilities.</p><p>This example illustrates how to use the ASPxLabel to identify that the grid was successfully updated. </p><p>A similar approach my be used with any other DevExpress ASP.NET control that can send callbacks (ASPxCallback, ASPxCallbackPanel, ASPxTreeList, ASPxComboBox and so on).</p>

<br/>


