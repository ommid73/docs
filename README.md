# GitHub Docs <!-- omid in toc -->
#!/bin/bash

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<html><head><title>Python: module siteinfo</title>
</head><body bgcolor="#f0f0f8">

<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="heading">
<tr bgcolor="#7799ee">
<td valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial">&nbsp;<br><big><big><strong>siteinfo</strong></big></big></font></td
><td align=right valign=bottom
><font color="#ffffff" face="helvetica, arial"><a href=".">index</a><br><a href="file:/home/jim/Files/TekDefense/TekDefense-Automater-Private/siteinfo.py">/home/jim/Files/TekDefense/TekDefense-Automater-Private/siteinfo.py</a></font></td></tr></table>
    <p><tt>The&nbsp;siteinfo.py&nbsp;module&nbsp;provides&nbsp;site&nbsp;lookup&nbsp;and&nbsp;result<br>
storage&nbsp;for&nbsp;those&nbsp;sites&nbsp;based&nbsp;on&nbsp;the&nbsp;sites.xml&nbsp;config<br>
file&nbsp;and&nbsp;the&nbsp;arguments&nbsp;sent&nbsp;in&nbsp;to&nbsp;the&nbsp;Automater.<br>
&nbsp;<br>
Class(es):<br>
<a href="#SiteFacade">SiteFacade</a>&nbsp;--&nbsp;Class&nbsp;used&nbsp;to&nbsp;run&nbsp;the&nbsp;automation&nbsp;necessary&nbsp;to&nbsp;retrieve<br>
site&nbsp;information&nbsp;and&nbsp;store&nbsp;results.<br>
<a href="#Site">Site</a>&nbsp;--&nbsp;Parent&nbsp;Class&nbsp;used&nbsp;to&nbsp;store&nbsp;sites&nbsp;and&nbsp;information&nbsp;retrieved.<br>
<a href="#SingleResultsSite">SingleResultsSite</a>&nbsp;--&nbsp;Class&nbsp;used&nbsp;to&nbsp;store&nbsp;information&nbsp;from&nbsp;a&nbsp;site&nbsp;that<br>
only&nbsp;has&nbsp;one&nbsp;result&nbsp;requested&nbsp;and&nbsp;discovered.<br>
<a href="#MultiResultsSite">MultiResultsSite</a>&nbsp;--&nbsp;Class&nbsp;used&nbsp;to&nbsp;store&nbsp;information&nbsp;from&nbsp;a&nbsp;site&nbsp;that<br>
has&nbsp;multiple&nbsp;results&nbsp;requested&nbsp;and&nbsp;discovered.<br>
<a href="#PostTransactionPositiveCapableSite">PostTransactionPositiveCapableSite</a>&nbsp;--&nbsp;Class&nbsp;used&nbsp;to&nbsp;store&nbsp;information<br>
from&nbsp;a&nbsp;site&nbsp;that&nbsp;has&nbsp;single&nbsp;or&nbsp;multiple&nbsp;results&nbsp;requested&nbsp;and&nbsp;discovered.<br>
This&nbsp;Class&nbsp;is&nbsp;utilized&nbsp;to&nbsp;post&nbsp;information&nbsp;to&nbsp;web&nbsp;sites&nbsp;if&nbsp;a&nbsp;post&nbsp;is<br>
required&nbsp;and&nbsp;requested&nbsp;via&nbsp;a&nbsp;--p&nbsp;argument&nbsp;utilized&nbsp;when&nbsp;the&nbsp;program&nbsp;is<br>
called.&nbsp;This&nbsp;Class&nbsp;expects&nbsp;to&nbsp;find&nbsp;the&nbsp;first&nbsp;regular&nbsp;expression&nbsp;listed<br>
in&nbsp;the&nbsp;sites.xml&nbsp;config&nbsp;file.&nbsp;If&nbsp;that&nbsp;regex&nbsp;is&nbsp;found,&nbsp;it&nbsp;tells&nbsp;the&nbsp;class<br>
that&nbsp;a&nbsp;post&nbsp;is&nbsp;necessary.<br>
<a href="#PostTransactionAPIKeySite">PostTransactionAPIKeySite</a>&nbsp;--&nbsp;Class&nbsp;used&nbsp;to&nbsp;store&nbsp;information&nbsp;from&nbsp;a<br>
site&nbsp;that&nbsp;has&nbsp;single&nbsp;or&nbsp;multiple&nbsp;results&nbsp;requested&nbsp;and&nbsp;discovered.&nbsp;This<br>
Class&nbsp;is&nbsp;utilized&nbsp;if&nbsp;an&nbsp;API&nbsp;key&nbsp;is&nbsp;provided&nbsp;in&nbsp;the&nbsp;sites.xml<br>
configuration&nbsp;file.<br>
&nbsp;<br>
Function(s):<br>
No&nbsp;global&nbsp;exportable&nbsp;functions&nbsp;are&nbsp;defined.<br>
&nbsp;<br>
Exception(s):<br>
No&nbsp;exceptions&nbsp;exported.</tt></p>
<p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#aa55cc">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Modules</strong></big></font></td></tr>
    
<tr><td bgcolor="#aa55cc"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><table width="100%" summary="list"><tr><td width="25%" valign=top><a href="re.html">re</a><br>
</td><td width="25%" valign=top><a href="time.html">time</a><br>
</td><td width="25%" valign=top><a href="urllib.html">urllib</a><br>
</td><td width="25%" valign=top><a href="urllib2.html">urllib2</a><br>
</td></tr></table></td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ee77aa">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Classes</strong></big></font></td></tr>
    
<tr><td bgcolor="#ee77aa"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl>
<dt><font face="helvetica, arial"><a href="__builtin__.html#object">__builtin__.object</a>
</font></dt><dd>
<dl>
<dt><font face="helvetica, arial"><a href="siteinfo.html#Site">Site</a>
</font></dt><dd>
<dl>
<dt><font face="helvetica, arial"><a href="siteinfo.html#MultiResultsSite">MultiResultsSite</a>
</font></dt><dt><font face="helvetica, arial"><a href="siteinfo.html#PostTransactionAPIKeySite">PostTransactionAPIKeySite</a>
</font></dt><dt><font face="helvetica, arial"><a href="siteinfo.html#PostTransactionPositiveCapableSite">PostTransactionPositiveCapableSite</a>
</font></dt><dt><font face="helvetica, arial"><a href="siteinfo.html#SingleResultsSite">SingleResultsSite</a>
</font></dt></dl>
</dd>
<dt><font face="helvetica, arial"><a href="siteinfo.html#SiteFacade">SiteFacade</a>
</font></dt></dl>
</dd>
</dl>
 <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="MultiResultsSite">class <strong>MultiResultsSite</strong></a>(<a href="siteinfo.html#Site">Site</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#MultiResultsSite">MultiResultsSite</a>&nbsp;inherits&nbsp;from&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;and&nbsp;represents<br>
a&nbsp;site&nbsp;that&nbsp;is&nbsp;being&nbsp;used&nbsp;that&nbsp;has&nbsp;multiple&nbsp;results&nbsp;returned.<br>
&nbsp;<br>
Public&nbsp;Method(s):<br>
addResults<br>
getContentList<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
_site<br>
_results<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="siteinfo.html#MultiResultsSite">MultiResultsSite</a></dd>
<dd><a href="siteinfo.html#Site">Site</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="MultiResultsSite-__init__"><strong>__init__</strong></a>(self, site)</dt><dd><tt>Class&nbsp;constructor.&nbsp;Assigns&nbsp;a&nbsp;site&nbsp;from&nbsp;the&nbsp;parameter&nbsp;into&nbsp;the&nbsp;_site<br>
instance&nbsp;variable.&nbsp;This&nbsp;is&nbsp;a&nbsp;play&nbsp;on&nbsp;the&nbsp;decorator&nbsp;pattern.<br>
&nbsp;<br>
Argument(s):<br>
site&nbsp;--&nbsp;the&nbsp;site&nbsp;that&nbsp;we&nbsp;will&nbsp;decorate.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-addResults"><strong>addResults</strong></a>(self, results, index)</dt><dd><tt>Assigns&nbsp;the&nbsp;argument&nbsp;to&nbsp;the&nbsp;_results&nbsp;instance&nbsp;variable&nbsp;to&nbsp;build<br>
the&nbsp;list&nbsp;or&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.&nbsp;Assign&nbsp;None&nbsp;to&nbsp;the<br>
_results&nbsp;instance&nbsp;variable&nbsp;if&nbsp;the&nbsp;argument&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
results&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
index&nbsp;--&nbsp;integer&nbsp;value&nbsp;representing&nbsp;the&nbsp;index&nbsp;of&nbsp;the&nbsp;result&nbsp;found.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-getContentList"><strong>getContentList</strong></a>(self, webcontent, index)</dt><dd><tt>Retrieves&nbsp;a&nbsp;list&nbsp;of&nbsp;information&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;sites&nbsp;defined<br>
in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;list&nbsp;of&nbsp;found&nbsp;information&nbsp;from&nbsp;the&nbsp;sites&nbsp;being&nbsp;used<br>
as&nbsp;resources&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;site&nbsp;cannot&nbsp;be&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
webcontent&nbsp;--&nbsp;actual&nbsp;content&nbsp;of&nbsp;the&nbsp;web&nbsp;page&nbsp;that's&nbsp;been&nbsp;returned<br>
from&nbsp;a&nbsp;request.<br>
index&nbsp;--&nbsp;the&nbsp;integer&nbsp;representing&nbsp;the&nbsp;index&nbsp;of&nbsp;the&nbsp;regex&nbsp;list.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;information&nbsp;found&nbsp;from&nbsp;a&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a&nbsp;resource.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="MultiResultsSite-getFullURL"><strong>getFullURL</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;FullURL&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-getImportantProperty"><strong>getImportantProperty</strong></a>(self, index)</dt><dd><tt>Gets&nbsp;the&nbsp;property&nbsp;information&nbsp;from&nbsp;the&nbsp;property&nbsp;value&nbsp;listed&nbsp;in&nbsp;the<br>
sites.xml&nbsp;file&nbsp;for&nbsp;that&nbsp;specific&nbsp;site&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;xml&nbsp;tag.<br>
This&nbsp;Method&nbsp;allows&nbsp;for&nbsp;the&nbsp;property&nbsp;that&nbsp;will&nbsp;be&nbsp;printed&nbsp;to&nbsp;be&nbsp;changed<br>
using&nbsp;the&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;return&nbsp;value&nbsp;listed&nbsp;in&nbsp;the&nbsp;property&nbsp;attribute&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
index&nbsp;--&nbsp;integer&nbsp;representing&nbsp;which&nbsp;important&nbsp;property&nbsp;is&nbsp;retrieved&nbsp;if<br>
more&nbsp;than&nbsp;one&nbsp;important&nbsp;property&nbsp;value&nbsp;is&nbsp;listed&nbsp;in&nbsp;the&nbsp;config&nbsp;file.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Multiple&nbsp;options&nbsp;--&nbsp;returns&nbsp;the&nbsp;return&nbsp;value&nbsp;of&nbsp;the&nbsp;property&nbsp;listed&nbsp;in<br>
the&nbsp;config&nbsp;file.&nbsp;Most&nbsp;likely&nbsp;a&nbsp;string&nbsp;or&nbsp;a&nbsp;list.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-getResults"><strong>getResults</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Results&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-getTarget"><strong>getTarget</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Target&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-getWebScrape"><strong>getWebScrape</strong></a>(self)</dt><dd><tt>Attempts&nbsp;to&nbsp;retrieve&nbsp;a&nbsp;string&nbsp;from&nbsp;a&nbsp;web&nbsp;site.&nbsp;String&nbsp;retrieved&nbsp;is<br>
the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;HTML&nbsp;markup.&nbsp;Requests&nbsp;via&nbsp;proxy&nbsp;if<br>
--proxy&nbsp;option&nbsp;was&nbsp;chosen&nbsp;during&nbsp;execution&nbsp;of&nbsp;the&nbsp;Automater.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;the<br>
HTML&nbsp;markup&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-postMessage"><strong>postMessage</strong></a>(self, message)</dt><dd><tt>Prints&nbsp;multiple&nbsp;messages&nbsp;to&nbsp;inform&nbsp;the&nbsp;user&nbsp;of&nbsp;progress.&nbsp;Assignes<br>
the&nbsp;_messagetopost&nbsp;instance&nbsp;variable&nbsp;to&nbsp;the&nbsp;message.&nbsp;Uses&nbsp;the<br>
MessageToPost&nbsp;property.<br>
&nbsp;<br>
Argument(s):<br>
message&nbsp;--&nbsp;string&nbsp;to&nbsp;be&nbsp;utilized&nbsp;as&nbsp;a&nbsp;message&nbsp;to&nbsp;post.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Class methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="MultiResultsSite-buildDictionaryFromXML"><strong>buildDictionaryFromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;dictionary<br>
from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config&nbsp;file.<br>
Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;dictionary&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
Dictionary&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-buildSiteFromXML"><strong>buildSiteFromXML</strong></a>(self, siteelement, webretrievedelay, proxy, targettype, target, useragent)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Utilizes&nbsp;the&nbsp;Class&nbsp;Methods&nbsp;within&nbsp;this&nbsp;Class&nbsp;to&nbsp;build&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
Returns&nbsp;a&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;defines&nbsp;results&nbsp;returned&nbsp;during&nbsp;the&nbsp;web<br>
retrieval&nbsp;investigations.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
webretrievedelay&nbsp;--&nbsp;the&nbsp;amount&nbsp;of&nbsp;seconds&nbsp;to&nbsp;wait&nbsp;between&nbsp;site&nbsp;retrieve<br>
calls.&nbsp;Default&nbsp;delay&nbsp;is&nbsp;2&nbsp;seconds.<br>
proxy&nbsp;--&nbsp;sets&nbsp;a&nbsp;proxy&nbsp;to&nbsp;use&nbsp;in&nbsp;the&nbsp;form&nbsp;of&nbsp;proxy.example.com:8080.<br>
targettype&nbsp;--&nbsp;the&nbsp;targettype&nbsp;as&nbsp;defined.&nbsp;Either&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
target&nbsp;--&nbsp;the&nbsp;target&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;to&nbsp;gather&nbsp;information&nbsp;on.<br>
useragent&nbsp;--&nbsp;the&nbsp;string&nbsp;utilized&nbsp;to&nbsp;represent&nbsp;the&nbsp;user-agent&nbsp;when<br>
web&nbsp;requests&nbsp;or&nbsp;submissions&nbsp;are&nbsp;made.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="MultiResultsSite-buildStringOrListfromXML"><strong>buildStringOrListfromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;string<br>
or&nbsp;list&nbsp;from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config<br>
file.&nbsp;Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;list&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found&nbsp;or&nbsp;a&nbsp;string&nbsp;of&nbsp;that&nbsp;entry&nbsp;if&nbsp;only<br>
one&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;is&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
List&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
string&nbsp;representing&nbsp;an&nbsp;entry&nbsp;key&nbsp;if&nbsp;only&nbsp;one&nbsp;is&nbsp;found<br>
within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><strong>APIKey</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;an&nbsp;APIKey&nbsp;was&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;APIKey&nbsp;using&nbsp;the<br>
_apikey&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;APIKey&nbsp;from&nbsp;the&nbsp;_apikey<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ErrorMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Error&nbsp;Message.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;error&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FriendlyName</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;friendly&nbsp;string&nbsp;name.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;friendly&nbsp;name&nbsp;for&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FullURL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Headers</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;Headers&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Headers&nbsp;using&nbsp;the<br>
_headers&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Headers&nbsp;from&nbsp;the&nbsp;_headers<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ImportantPropertyString</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Important&nbsp;Property<br>
that&nbsp;the&nbsp;user&nbsp;wants&nbsp;the&nbsp;site&nbsp;to&nbsp;report.&nbsp;This&nbsp;is&nbsp;set&nbsp;using<br>
the&nbsp;sites.xml&nbsp;config&nbsp;file&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;XML&nbsp;tag.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;important&nbsp;property&nbsp;of&nbsp;the&nbsp;site<br>
that&nbsp;needs&nbsp;to&nbsp;be&nbsp;reported.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>MessageToPost</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;the&nbsp;user.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Params</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;web&nbsp;Parameters&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Parameters&nbsp;using&nbsp;the<br>
_params&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Parameters&nbsp;from&nbsp;the&nbsp;_params<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Proxy</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>RegEx</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;regular&nbsp;expression<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;regex&nbsp;used&nbsp;to&nbsp;find&nbsp;info&nbsp;on&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ReportStringForResult</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;report&nbsp;string&nbsp;tag&nbsp;that<br>
precedes&nbsp;reporting&nbsp;information&nbsp;so&nbsp;the&nbsp;user&nbsp;knows&nbsp;what<br>
specifics&nbsp;are&nbsp;being&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting&nbsp;information.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Results</strong></dt>
<dd><tt>Checks&nbsp;the&nbsp;instance&nbsp;variable&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
Returns&nbsp;_results&nbsp;(the&nbsp;results&nbsp;list)&nbsp;or&nbsp;None&nbsp;if&nbsp;it&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;discovered&nbsp;from&nbsp;the&nbsp;site&nbsp;being&nbsp;investigated.<br>
None&nbsp;--&nbsp;if&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Target</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;target&nbsp;being&nbsp;investigated.<br>
The&nbsp;string&nbsp;may&nbsp;be&nbsp;an&nbsp;IP&nbsp;Address,&nbsp;MD5&nbsp;hash,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Target&nbsp;from&nbsp;the&nbsp;_target<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>TargetType</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;target&nbsp;type&nbsp;information&nbsp;whether&nbsp;that&nbsp;be&nbsp;ip,<br>
md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;defined&nbsp;as&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>URL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Domain&nbsp;URL&nbsp;which&nbsp;is<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;URL&nbsp;of&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserAgent</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;user-agent&nbsp;that&nbsp;will<br>
be&nbsp;used&nbsp;when&nbsp;requesting&nbsp;or&nbsp;submitting&nbsp;information&nbsp;to<br>
a&nbsp;web&nbsp;site.&nbsp;This&nbsp;is&nbsp;a&nbsp;user-provided&nbsp;string&nbsp;implemented<br>
on&nbsp;the&nbsp;command&nbsp;line&nbsp;at&nbsp;execution&nbsp;or&nbsp;provided&nbsp;by&nbsp;default<br>
if&nbsp;not&nbsp;added&nbsp;during&nbsp;execution.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;UserAgent&nbsp;from&nbsp;the&nbsp;_userAgent<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>WebRetrieveDelay</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;number&nbsp;of<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;delayed&nbsp;between&nbsp;site&nbsp;retrievals.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;an&nbsp;integer&nbsp;that&nbsp;is&nbsp;the&nbsp;delay&nbsp;in<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;between&nbsp;each&nbsp;web&nbsp;site&nbsp;retrieval.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="PostTransactionAPIKeySite">class <strong>PostTransactionAPIKeySite</strong></a>(<a href="siteinfo.html#Site">Site</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#PostTransactionAPIKeySite">PostTransactionAPIKeySite</a>&nbsp;inherits&nbsp;from&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a><br>
and&nbsp;represents&nbsp;a&nbsp;site&nbsp;that&nbsp;needs&nbsp;an&nbsp;API&nbsp;Key&nbsp;for&nbsp;discovering<br>
information.<br>
&nbsp;<br>
Public&nbsp;Method(s):<br>
addMultiResults<br>
getContentList<br>
submitPost<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
_site<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="siteinfo.html#PostTransactionAPIKeySite">PostTransactionAPIKeySite</a></dd>
<dd><a href="siteinfo.html#Site">Site</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="PostTransactionAPIKeySite-__init__"><strong>__init__</strong></a>(self, site)</dt><dd><tt>Class&nbsp;constructor.&nbsp;Assigns&nbsp;a&nbsp;site&nbsp;from&nbsp;the&nbsp;parameter&nbsp;into&nbsp;the&nbsp;_site<br>
instance&nbsp;variable.&nbsp;This&nbsp;is&nbsp;a&nbsp;play&nbsp;on&nbsp;the&nbsp;decorator&nbsp;pattern.<br>
&nbsp;<br>
Argument(s):<br>
site&nbsp;--&nbsp;the&nbsp;site&nbsp;that&nbsp;we&nbsp;will&nbsp;decorate.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-addMultiResults"><strong>addMultiResults</strong></a>(self, results, index)</dt><dd><tt>Assigns&nbsp;the&nbsp;argument&nbsp;to&nbsp;the&nbsp;_results&nbsp;instance&nbsp;variable&nbsp;to&nbsp;build<br>
the&nbsp;list&nbsp;or&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.&nbsp;Assign&nbsp;None&nbsp;to&nbsp;the<br>
_results&nbsp;instance&nbsp;variable&nbsp;if&nbsp;the&nbsp;argument&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
results&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
index&nbsp;--&nbsp;integer&nbsp;value&nbsp;representing&nbsp;the&nbsp;index&nbsp;of&nbsp;the&nbsp;result&nbsp;found.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-getContentList"><strong>getContentList</strong></a>(self, content, index<font color="#909090">=-1</font>)</dt><dd><tt>Retrieves&nbsp;a&nbsp;list&nbsp;of&nbsp;information&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;sites&nbsp;defined<br>
in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;list&nbsp;of&nbsp;found&nbsp;information&nbsp;from&nbsp;the&nbsp;sites&nbsp;being&nbsp;used<br>
as&nbsp;resources&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;site&nbsp;cannot&nbsp;be&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
content&nbsp;--&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;web&nbsp;site&nbsp;being&nbsp;used<br>
as&nbsp;a&nbsp;resource.<br>
index&nbsp;--&nbsp;the&nbsp;integer&nbsp;representing&nbsp;the&nbsp;index&nbsp;of&nbsp;the&nbsp;regex&nbsp;list.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;information&nbsp;found&nbsp;from&nbsp;a&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a&nbsp;resource.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-submitPost"><strong>submitPost</strong></a>(self, raw_params, headers)</dt><dd><tt>Submits&nbsp;information&nbsp;to&nbsp;a&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a&nbsp;resource&nbsp;that<br>
requires&nbsp;a&nbsp;post&nbsp;of&nbsp;information.&nbsp;Submits&nbsp;via&nbsp;proxy&nbsp;if&nbsp;--proxy<br>
option&nbsp;was&nbsp;chosen&nbsp;during&nbsp;execution&nbsp;of&nbsp;the&nbsp;Automater.<br>
Returns&nbsp;a&nbsp;string&nbsp;that&nbsp;contains&nbsp;entire&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a<br>
resource&nbsp;including&nbsp;HTML&nbsp;markup&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
raw_params&nbsp;--&nbsp;string&nbsp;info&nbsp;detailing&nbsp;parameters&nbsp;provided&nbsp;from<br>
sites.xml&nbsp;configuration&nbsp;file&nbsp;in&nbsp;the&nbsp;params&nbsp;XML&nbsp;tag.<br>
headers&nbsp;--&nbsp;string&nbsp;info&nbsp;detailing&nbsp;headers&nbsp;provided&nbsp;from<br>
sites.xml&nbsp;configuration&nbsp;file&nbsp;in&nbsp;the&nbsp;headers&nbsp;XML&nbsp;tag.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;contains&nbsp;entire&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a<br>
resource&nbsp;including&nbsp;HTML&nbsp;markup&nbsp;information.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="PostTransactionAPIKeySite-addResults"><strong>addResults</strong></a>(self, results)</dt><dd><tt>Assigns&nbsp;the&nbsp;argument&nbsp;to&nbsp;the&nbsp;_results&nbsp;instance&nbsp;variable&nbsp;to&nbsp;build<br>
the&nbsp;list&nbsp;or&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.&nbsp;Assign&nbsp;None&nbsp;to&nbsp;the<br>
_results&nbsp;instance&nbsp;variable&nbsp;if&nbsp;the&nbsp;argument&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
results&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-getFullURL"><strong>getFullURL</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;FullURL&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-getImportantProperty"><strong>getImportantProperty</strong></a>(self, index)</dt><dd><tt>Gets&nbsp;the&nbsp;property&nbsp;information&nbsp;from&nbsp;the&nbsp;property&nbsp;value&nbsp;listed&nbsp;in&nbsp;the<br>
sites.xml&nbsp;file&nbsp;for&nbsp;that&nbsp;specific&nbsp;site&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;xml&nbsp;tag.<br>
This&nbsp;Method&nbsp;allows&nbsp;for&nbsp;the&nbsp;property&nbsp;that&nbsp;will&nbsp;be&nbsp;printed&nbsp;to&nbsp;be&nbsp;changed<br>
using&nbsp;the&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;return&nbsp;value&nbsp;listed&nbsp;in&nbsp;the&nbsp;property&nbsp;attribute&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
index&nbsp;--&nbsp;integer&nbsp;representing&nbsp;which&nbsp;important&nbsp;property&nbsp;is&nbsp;retrieved&nbsp;if<br>
more&nbsp;than&nbsp;one&nbsp;important&nbsp;property&nbsp;value&nbsp;is&nbsp;listed&nbsp;in&nbsp;the&nbsp;config&nbsp;file.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Multiple&nbsp;options&nbsp;--&nbsp;returns&nbsp;the&nbsp;return&nbsp;value&nbsp;of&nbsp;the&nbsp;property&nbsp;listed&nbsp;in<br>
the&nbsp;config&nbsp;file.&nbsp;Most&nbsp;likely&nbsp;a&nbsp;string&nbsp;or&nbsp;a&nbsp;list.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-getResults"><strong>getResults</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Results&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-getTarget"><strong>getTarget</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Target&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-getWebScrape"><strong>getWebScrape</strong></a>(self)</dt><dd><tt>Attempts&nbsp;to&nbsp;retrieve&nbsp;a&nbsp;string&nbsp;from&nbsp;a&nbsp;web&nbsp;site.&nbsp;String&nbsp;retrieved&nbsp;is<br>
the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;HTML&nbsp;markup.&nbsp;Requests&nbsp;via&nbsp;proxy&nbsp;if<br>
--proxy&nbsp;option&nbsp;was&nbsp;chosen&nbsp;during&nbsp;execution&nbsp;of&nbsp;the&nbsp;Automater.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;the<br>
HTML&nbsp;markup&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-postMessage"><strong>postMessage</strong></a>(self, message)</dt><dd><tt>Prints&nbsp;multiple&nbsp;messages&nbsp;to&nbsp;inform&nbsp;the&nbsp;user&nbsp;of&nbsp;progress.&nbsp;Assignes<br>
the&nbsp;_messagetopost&nbsp;instance&nbsp;variable&nbsp;to&nbsp;the&nbsp;message.&nbsp;Uses&nbsp;the<br>
MessageToPost&nbsp;property.<br>
&nbsp;<br>
Argument(s):<br>
message&nbsp;--&nbsp;string&nbsp;to&nbsp;be&nbsp;utilized&nbsp;as&nbsp;a&nbsp;message&nbsp;to&nbsp;post.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Class methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="PostTransactionAPIKeySite-buildDictionaryFromXML"><strong>buildDictionaryFromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;dictionary<br>
from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config&nbsp;file.<br>
Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;dictionary&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
Dictionary&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-buildSiteFromXML"><strong>buildSiteFromXML</strong></a>(self, siteelement, webretrievedelay, proxy, targettype, target, useragent)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Utilizes&nbsp;the&nbsp;Class&nbsp;Methods&nbsp;within&nbsp;this&nbsp;Class&nbsp;to&nbsp;build&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
Returns&nbsp;a&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;defines&nbsp;results&nbsp;returned&nbsp;during&nbsp;the&nbsp;web<br>
retrieval&nbsp;investigations.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
webretrievedelay&nbsp;--&nbsp;the&nbsp;amount&nbsp;of&nbsp;seconds&nbsp;to&nbsp;wait&nbsp;between&nbsp;site&nbsp;retrieve<br>
calls.&nbsp;Default&nbsp;delay&nbsp;is&nbsp;2&nbsp;seconds.<br>
proxy&nbsp;--&nbsp;sets&nbsp;a&nbsp;proxy&nbsp;to&nbsp;use&nbsp;in&nbsp;the&nbsp;form&nbsp;of&nbsp;proxy.example.com:8080.<br>
targettype&nbsp;--&nbsp;the&nbsp;targettype&nbsp;as&nbsp;defined.&nbsp;Either&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
target&nbsp;--&nbsp;the&nbsp;target&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;to&nbsp;gather&nbsp;information&nbsp;on.<br>
useragent&nbsp;--&nbsp;the&nbsp;string&nbsp;utilized&nbsp;to&nbsp;represent&nbsp;the&nbsp;user-agent&nbsp;when<br>
web&nbsp;requests&nbsp;or&nbsp;submissions&nbsp;are&nbsp;made.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="PostTransactionAPIKeySite-buildStringOrListfromXML"><strong>buildStringOrListfromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;string<br>
or&nbsp;list&nbsp;from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config<br>
file.&nbsp;Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;list&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found&nbsp;or&nbsp;a&nbsp;string&nbsp;of&nbsp;that&nbsp;entry&nbsp;if&nbsp;only<br>
one&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;is&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
List&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
string&nbsp;representing&nbsp;an&nbsp;entry&nbsp;key&nbsp;if&nbsp;only&nbsp;one&nbsp;is&nbsp;found<br>
within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><strong>APIKey</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;an&nbsp;APIKey&nbsp;was&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;APIKey&nbsp;using&nbsp;the<br>
_apikey&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;APIKey&nbsp;from&nbsp;the&nbsp;_apikey<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ErrorMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Error&nbsp;Message.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;error&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FriendlyName</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;friendly&nbsp;string&nbsp;name.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;friendly&nbsp;name&nbsp;for&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FullURL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Headers</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;Headers&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Headers&nbsp;using&nbsp;the<br>
_headers&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Headers&nbsp;from&nbsp;the&nbsp;_headers<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ImportantPropertyString</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Important&nbsp;Property<br>
that&nbsp;the&nbsp;user&nbsp;wants&nbsp;the&nbsp;site&nbsp;to&nbsp;report.&nbsp;This&nbsp;is&nbsp;set&nbsp;using<br>
the&nbsp;sites.xml&nbsp;config&nbsp;file&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;XML&nbsp;tag.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;important&nbsp;property&nbsp;of&nbsp;the&nbsp;site<br>
that&nbsp;needs&nbsp;to&nbsp;be&nbsp;reported.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>MessageToPost</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;the&nbsp;user.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Params</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;web&nbsp;Parameters&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Parameters&nbsp;using&nbsp;the<br>
_params&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Parameters&nbsp;from&nbsp;the&nbsp;_params<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Proxy</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>RegEx</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;regular&nbsp;expression<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;regex&nbsp;used&nbsp;to&nbsp;find&nbsp;info&nbsp;on&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ReportStringForResult</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;report&nbsp;string&nbsp;tag&nbsp;that<br>
precedes&nbsp;reporting&nbsp;information&nbsp;so&nbsp;the&nbsp;user&nbsp;knows&nbsp;what<br>
specifics&nbsp;are&nbsp;being&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting&nbsp;information.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Results</strong></dt>
<dd><tt>Checks&nbsp;the&nbsp;instance&nbsp;variable&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
Returns&nbsp;_results&nbsp;(the&nbsp;results&nbsp;list)&nbsp;or&nbsp;None&nbsp;if&nbsp;it&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;discovered&nbsp;from&nbsp;the&nbsp;site&nbsp;being&nbsp;investigated.<br>
None&nbsp;--&nbsp;if&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Target</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;target&nbsp;being&nbsp;investigated.<br>
The&nbsp;string&nbsp;may&nbsp;be&nbsp;an&nbsp;IP&nbsp;Address,&nbsp;MD5&nbsp;hash,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Target&nbsp;from&nbsp;the&nbsp;_target<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>TargetType</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;target&nbsp;type&nbsp;information&nbsp;whether&nbsp;that&nbsp;be&nbsp;ip,<br>
md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;defined&nbsp;as&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>URL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Domain&nbsp;URL&nbsp;which&nbsp;is<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;URL&nbsp;of&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserAgent</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;user-agent&nbsp;that&nbsp;will<br>
be&nbsp;used&nbsp;when&nbsp;requesting&nbsp;or&nbsp;submitting&nbsp;information&nbsp;to<br>
a&nbsp;web&nbsp;site.&nbsp;This&nbsp;is&nbsp;a&nbsp;user-provided&nbsp;string&nbsp;implemented<br>
on&nbsp;the&nbsp;command&nbsp;line&nbsp;at&nbsp;execution&nbsp;or&nbsp;provided&nbsp;by&nbsp;default<br>
if&nbsp;not&nbsp;added&nbsp;during&nbsp;execution.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;UserAgent&nbsp;from&nbsp;the&nbsp;_userAgent<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>WebRetrieveDelay</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;number&nbsp;of<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;delayed&nbsp;between&nbsp;site&nbsp;retrievals.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;an&nbsp;integer&nbsp;that&nbsp;is&nbsp;the&nbsp;delay&nbsp;in<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;between&nbsp;each&nbsp;web&nbsp;site&nbsp;retrieval.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="PostTransactionPositiveCapableSite">class <strong>PostTransactionPositiveCapableSite</strong></a>(<a href="siteinfo.html#Site">Site</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#PostTransactionPositiveCapableSite">PostTransactionPositiveCapableSite</a>&nbsp;inherits&nbsp;from&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a><br>
and&nbsp;represents&nbsp;a&nbsp;site&nbsp;that&nbsp;may&nbsp;need&nbsp;to&nbsp;post&nbsp;information.<br>
&nbsp;<br>
Public&nbsp;Method(s):<br>
addMultiResults<br>
getContentList<br>
getContent<br>
postIsNecessary<br>
submitPost<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
_site<br>
_postByDefault<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="siteinfo.html#PostTransactionPositiveCapableSite">PostTransactionPositiveCapableSite</a></dd>
<dd><a href="siteinfo.html#Site">Site</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="PostTransactionPositiveCapableSite-__init__"><strong>__init__</strong></a>(self, site, postbydefault)</dt><dd><tt>Class&nbsp;constructor.&nbsp;Assigns&nbsp;a&nbsp;site&nbsp;from&nbsp;the&nbsp;parameter&nbsp;into&nbsp;the&nbsp;_site<br>
instance&nbsp;variable.&nbsp;This&nbsp;is&nbsp;a&nbsp;play&nbsp;on&nbsp;the&nbsp;decorator&nbsp;pattern.&nbsp;Also<br>
assigns&nbsp;the&nbsp;postbydefault&nbsp;parameter&nbsp;to&nbsp;the&nbsp;_postByDefault&nbsp;instance<br>
variable&nbsp;to&nbsp;determine&nbsp;if&nbsp;the&nbsp;Automater&nbsp;should&nbsp;post&nbsp;information<br>
to&nbsp;a&nbsp;site.&nbsp;By&nbsp;default&nbsp;Automater&nbsp;will&nbsp;NOT&nbsp;post&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
site&nbsp;--&nbsp;the&nbsp;site&nbsp;that&nbsp;we&nbsp;will&nbsp;decorate.<br>
postbydefault&nbsp;--&nbsp;a&nbsp;Boolean&nbsp;representing&nbsp;whether&nbsp;a&nbsp;post&nbsp;will&nbsp;occur.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-addMultiResults"><strong>addMultiResults</strong></a>(self, results, index)</dt><dd><tt>Assigns&nbsp;the&nbsp;argument&nbsp;to&nbsp;the&nbsp;_results&nbsp;instance&nbsp;variable&nbsp;to&nbsp;build<br>
the&nbsp;list&nbsp;or&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.&nbsp;Assign&nbsp;None&nbsp;to&nbsp;the<br>
_results&nbsp;instance&nbsp;variable&nbsp;if&nbsp;the&nbsp;argument&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
results&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
index&nbsp;--&nbsp;integer&nbsp;value&nbsp;representing&nbsp;the&nbsp;index&nbsp;of&nbsp;the&nbsp;result&nbsp;found.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-getContent"><strong>getContent</strong></a>(self)</dt><dd><tt>Attempts&nbsp;to&nbsp;retrieve&nbsp;a&nbsp;string&nbsp;from&nbsp;a&nbsp;web&nbsp;site.&nbsp;String&nbsp;retrieved&nbsp;is<br>
the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;HTML&nbsp;markup.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;the<br>
HTML&nbsp;markup&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-getContentList"><strong>getContentList</strong></a>(self, content, index<font color="#909090">=-1</font>)</dt><dd><tt>Retrieves&nbsp;a&nbsp;list&nbsp;of&nbsp;information&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;sites&nbsp;defined<br>
in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;list&nbsp;of&nbsp;found&nbsp;information&nbsp;from&nbsp;the&nbsp;sites&nbsp;being&nbsp;used<br>
as&nbsp;resources&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;site&nbsp;cannot&nbsp;be&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
content&nbsp;--&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;web&nbsp;site&nbsp;being&nbsp;used<br>
as&nbsp;a&nbsp;resource.<br>
index&nbsp;--&nbsp;the&nbsp;integer&nbsp;representing&nbsp;the&nbsp;index&nbsp;of&nbsp;the&nbsp;regex&nbsp;list.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;information&nbsp;found&nbsp;from&nbsp;a&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a&nbsp;resource.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-postIsNecessary"><strong>postIsNecessary</strong></a>(self, regex, content)</dt><dd><tt>Checks&nbsp;to&nbsp;determine&nbsp;if&nbsp;the&nbsp;user&nbsp;wants&nbsp;the&nbsp;Automater&nbsp;to&nbsp;post&nbsp;information<br>
if&nbsp;the&nbsp;site&nbsp;takes&nbsp;a&nbsp;post.&nbsp;The&nbsp;user&nbsp;does&nbsp;this&nbsp;through&nbsp;the&nbsp;argument<br>
switch&nbsp;--p.&nbsp;By&nbsp;default&nbsp;this&nbsp;is&nbsp;False.&nbsp;If&nbsp;the&nbsp;regex&nbsp;given&nbsp;is&nbsp;found<br>
on&nbsp;the&nbsp;site,&nbsp;and&nbsp;a&nbsp;post&nbsp;is&nbsp;requested,&nbsp;a&nbsp;post&nbsp;will&nbsp;be&nbsp;attempted.<br>
Returns&nbsp;True&nbsp;if&nbsp;--p&nbsp;is&nbsp;used&nbsp;and&nbsp;a&nbsp;regex&nbsp;is&nbsp;found&nbsp;on&nbsp;the&nbsp;site,&nbsp;else<br>
return&nbsp;False.<br>
&nbsp;<br>
Argument(s):<br>
regex&nbsp;--&nbsp;string&nbsp;regex&nbsp;that&nbsp;will&nbsp;be&nbsp;searched&nbsp;for&nbsp;on&nbsp;the&nbsp;web&nbsp;site&nbsp;used<br>
as&nbsp;a&nbsp;resource.<br>
content&nbsp;--&nbsp;string&nbsp;that&nbsp;contains&nbsp;entire&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a<br>
resource&nbsp;including&nbsp;HTML&nbsp;markup&nbsp;information.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Boolean.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-submitPost"><strong>submitPost</strong></a>(self, raw_params, headers)</dt><dd><tt>Submits&nbsp;information&nbsp;to&nbsp;a&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a&nbsp;resource&nbsp;that<br>
requires&nbsp;a&nbsp;post&nbsp;of&nbsp;information.&nbsp;Submits&nbsp;via&nbsp;proxy&nbsp;if&nbsp;--proxy<br>
option&nbsp;was&nbsp;chosen&nbsp;during&nbsp;execution&nbsp;of&nbsp;the&nbsp;Automater.<br>
Returns&nbsp;a&nbsp;string&nbsp;that&nbsp;contains&nbsp;entire&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a<br>
resource&nbsp;including&nbsp;HTML&nbsp;markup&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
raw_params&nbsp;--&nbsp;string&nbsp;info&nbsp;detailing&nbsp;parameters&nbsp;provided&nbsp;from<br>
sites.xml&nbsp;configuration&nbsp;file&nbsp;in&nbsp;the&nbsp;params&nbsp;XML&nbsp;tag.<br>
headers&nbsp;--&nbsp;string&nbsp;info&nbsp;detailing&nbsp;headers&nbsp;provided&nbsp;from<br>
sites.xml&nbsp;configuration&nbsp;file&nbsp;in&nbsp;the&nbsp;headers&nbsp;XML&nbsp;tag.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;contains&nbsp;entire&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a<br>
resource&nbsp;including&nbsp;HTML&nbsp;markup&nbsp;information.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="PostTransactionPositiveCapableSite-addResults"><strong>addResults</strong></a>(self, results)</dt><dd><tt>Assigns&nbsp;the&nbsp;argument&nbsp;to&nbsp;the&nbsp;_results&nbsp;instance&nbsp;variable&nbsp;to&nbsp;build<br>
the&nbsp;list&nbsp;or&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.&nbsp;Assign&nbsp;None&nbsp;to&nbsp;the<br>
_results&nbsp;instance&nbsp;variable&nbsp;if&nbsp;the&nbsp;argument&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
results&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-getFullURL"><strong>getFullURL</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;FullURL&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-getImportantProperty"><strong>getImportantProperty</strong></a>(self, index)</dt><dd><tt>Gets&nbsp;the&nbsp;property&nbsp;information&nbsp;from&nbsp;the&nbsp;property&nbsp;value&nbsp;listed&nbsp;in&nbsp;the<br>
sites.xml&nbsp;file&nbsp;for&nbsp;that&nbsp;specific&nbsp;site&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;xml&nbsp;tag.<br>
This&nbsp;Method&nbsp;allows&nbsp;for&nbsp;the&nbsp;property&nbsp;that&nbsp;will&nbsp;be&nbsp;printed&nbsp;to&nbsp;be&nbsp;changed<br>
using&nbsp;the&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;return&nbsp;value&nbsp;listed&nbsp;in&nbsp;the&nbsp;property&nbsp;attribute&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
index&nbsp;--&nbsp;integer&nbsp;representing&nbsp;which&nbsp;important&nbsp;property&nbsp;is&nbsp;retrieved&nbsp;if<br>
more&nbsp;than&nbsp;one&nbsp;important&nbsp;property&nbsp;value&nbsp;is&nbsp;listed&nbsp;in&nbsp;the&nbsp;config&nbsp;file.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Multiple&nbsp;options&nbsp;--&nbsp;returns&nbsp;the&nbsp;return&nbsp;value&nbsp;of&nbsp;the&nbsp;property&nbsp;listed&nbsp;in<br>
the&nbsp;config&nbsp;file.&nbsp;Most&nbsp;likely&nbsp;a&nbsp;string&nbsp;or&nbsp;a&nbsp;list.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-getResults"><strong>getResults</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Results&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-getTarget"><strong>getTarget</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Target&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-getWebScrape"><strong>getWebScrape</strong></a>(self)</dt><dd><tt>Attempts&nbsp;to&nbsp;retrieve&nbsp;a&nbsp;string&nbsp;from&nbsp;a&nbsp;web&nbsp;site.&nbsp;String&nbsp;retrieved&nbsp;is<br>
the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;HTML&nbsp;markup.&nbsp;Requests&nbsp;via&nbsp;proxy&nbsp;if<br>
--proxy&nbsp;option&nbsp;was&nbsp;chosen&nbsp;during&nbsp;execution&nbsp;of&nbsp;the&nbsp;Automater.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;the<br>
HTML&nbsp;markup&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-postMessage"><strong>postMessage</strong></a>(self, message)</dt><dd><tt>Prints&nbsp;multiple&nbsp;messages&nbsp;to&nbsp;inform&nbsp;the&nbsp;user&nbsp;of&nbsp;progress.&nbsp;Assignes<br>
the&nbsp;_messagetopost&nbsp;instance&nbsp;variable&nbsp;to&nbsp;the&nbsp;message.&nbsp;Uses&nbsp;the<br>
MessageToPost&nbsp;property.<br>
&nbsp;<br>
Argument(s):<br>
message&nbsp;--&nbsp;string&nbsp;to&nbsp;be&nbsp;utilized&nbsp;as&nbsp;a&nbsp;message&nbsp;to&nbsp;post.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Class methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="PostTransactionPositiveCapableSite-buildDictionaryFromXML"><strong>buildDictionaryFromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;dictionary<br>
from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config&nbsp;file.<br>
Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;dictionary&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
Dictionary&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-buildSiteFromXML"><strong>buildSiteFromXML</strong></a>(self, siteelement, webretrievedelay, proxy, targettype, target, useragent)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Utilizes&nbsp;the&nbsp;Class&nbsp;Methods&nbsp;within&nbsp;this&nbsp;Class&nbsp;to&nbsp;build&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
Returns&nbsp;a&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;defines&nbsp;results&nbsp;returned&nbsp;during&nbsp;the&nbsp;web<br>
retrieval&nbsp;investigations.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
webretrievedelay&nbsp;--&nbsp;the&nbsp;amount&nbsp;of&nbsp;seconds&nbsp;to&nbsp;wait&nbsp;between&nbsp;site&nbsp;retrieve<br>
calls.&nbsp;Default&nbsp;delay&nbsp;is&nbsp;2&nbsp;seconds.<br>
proxy&nbsp;--&nbsp;sets&nbsp;a&nbsp;proxy&nbsp;to&nbsp;use&nbsp;in&nbsp;the&nbsp;form&nbsp;of&nbsp;proxy.example.com:8080.<br>
targettype&nbsp;--&nbsp;the&nbsp;targettype&nbsp;as&nbsp;defined.&nbsp;Either&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
target&nbsp;--&nbsp;the&nbsp;target&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;to&nbsp;gather&nbsp;information&nbsp;on.<br>
useragent&nbsp;--&nbsp;the&nbsp;string&nbsp;utilized&nbsp;to&nbsp;represent&nbsp;the&nbsp;user-agent&nbsp;when<br>
web&nbsp;requests&nbsp;or&nbsp;submissions&nbsp;are&nbsp;made.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="PostTransactionPositiveCapableSite-buildStringOrListfromXML"><strong>buildStringOrListfromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;string<br>
or&nbsp;list&nbsp;from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config<br>
file.&nbsp;Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;list&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found&nbsp;or&nbsp;a&nbsp;string&nbsp;of&nbsp;that&nbsp;entry&nbsp;if&nbsp;only<br>
one&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;is&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
List&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
string&nbsp;representing&nbsp;an&nbsp;entry&nbsp;key&nbsp;if&nbsp;only&nbsp;one&nbsp;is&nbsp;found<br>
within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><strong>APIKey</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;an&nbsp;APIKey&nbsp;was&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;APIKey&nbsp;using&nbsp;the<br>
_apikey&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;APIKey&nbsp;from&nbsp;the&nbsp;_apikey<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ErrorMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Error&nbsp;Message.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;error&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FriendlyName</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;friendly&nbsp;string&nbsp;name.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;friendly&nbsp;name&nbsp;for&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FullURL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Headers</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;Headers&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Headers&nbsp;using&nbsp;the<br>
_headers&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Headers&nbsp;from&nbsp;the&nbsp;_headers<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ImportantPropertyString</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Important&nbsp;Property<br>
that&nbsp;the&nbsp;user&nbsp;wants&nbsp;the&nbsp;site&nbsp;to&nbsp;report.&nbsp;This&nbsp;is&nbsp;set&nbsp;using<br>
the&nbsp;sites.xml&nbsp;config&nbsp;file&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;XML&nbsp;tag.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;important&nbsp;property&nbsp;of&nbsp;the&nbsp;site<br>
that&nbsp;needs&nbsp;to&nbsp;be&nbsp;reported.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>MessageToPost</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;the&nbsp;user.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Params</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;web&nbsp;Parameters&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Parameters&nbsp;using&nbsp;the<br>
_params&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Parameters&nbsp;from&nbsp;the&nbsp;_params<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Proxy</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>RegEx</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;regular&nbsp;expression<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;regex&nbsp;used&nbsp;to&nbsp;find&nbsp;info&nbsp;on&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ReportStringForResult</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;report&nbsp;string&nbsp;tag&nbsp;that<br>
precedes&nbsp;reporting&nbsp;information&nbsp;so&nbsp;the&nbsp;user&nbsp;knows&nbsp;what<br>
specifics&nbsp;are&nbsp;being&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting&nbsp;information.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Results</strong></dt>
<dd><tt>Checks&nbsp;the&nbsp;instance&nbsp;variable&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
Returns&nbsp;_results&nbsp;(the&nbsp;results&nbsp;list)&nbsp;or&nbsp;None&nbsp;if&nbsp;it&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;discovered&nbsp;from&nbsp;the&nbsp;site&nbsp;being&nbsp;investigated.<br>
None&nbsp;--&nbsp;if&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Target</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;target&nbsp;being&nbsp;investigated.<br>
The&nbsp;string&nbsp;may&nbsp;be&nbsp;an&nbsp;IP&nbsp;Address,&nbsp;MD5&nbsp;hash,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Target&nbsp;from&nbsp;the&nbsp;_target<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>TargetType</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;target&nbsp;type&nbsp;information&nbsp;whether&nbsp;that&nbsp;be&nbsp;ip,<br>
md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;defined&nbsp;as&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>URL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Domain&nbsp;URL&nbsp;which&nbsp;is<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;URL&nbsp;of&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserAgent</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;user-agent&nbsp;that&nbsp;will<br>
be&nbsp;used&nbsp;when&nbsp;requesting&nbsp;or&nbsp;submitting&nbsp;information&nbsp;to<br>
a&nbsp;web&nbsp;site.&nbsp;This&nbsp;is&nbsp;a&nbsp;user-provided&nbsp;string&nbsp;implemented<br>
on&nbsp;the&nbsp;command&nbsp;line&nbsp;at&nbsp;execution&nbsp;or&nbsp;provided&nbsp;by&nbsp;default<br>
if&nbsp;not&nbsp;added&nbsp;during&nbsp;execution.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;UserAgent&nbsp;from&nbsp;the&nbsp;_userAgent<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>WebRetrieveDelay</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;number&nbsp;of<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;delayed&nbsp;between&nbsp;site&nbsp;retrievals.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;an&nbsp;integer&nbsp;that&nbsp;is&nbsp;the&nbsp;delay&nbsp;in<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;between&nbsp;each&nbsp;web&nbsp;site&nbsp;retrieval.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="SingleResultsSite">class <strong>SingleResultsSite</strong></a>(<a href="siteinfo.html#Site">Site</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#SingleResultsSite">SingleResultsSite</a>&nbsp;inherits&nbsp;from&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;and&nbsp;represents<br>
a&nbsp;site&nbsp;that&nbsp;is&nbsp;being&nbsp;used&nbsp;that&nbsp;has&nbsp;a&nbsp;single&nbsp;result&nbsp;returned.<br>
&nbsp;<br>
Public&nbsp;Method(s):<br>
getContentList<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
_site<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%"><dl><dt>Method resolution order:</dt>
<dd><a href="siteinfo.html#SingleResultsSite">SingleResultsSite</a></dd>
<dd><a href="siteinfo.html#Site">Site</a></dd>
<dd><a href="__builtin__.html#object">__builtin__.object</a></dd>
</dl>
<hr>
Methods defined here:<br>
<dl><dt><a name="SingleResultsSite-__init__"><strong>__init__</strong></a>(self, site)</dt><dd><tt>Class&nbsp;constructor.&nbsp;Assigns&nbsp;a&nbsp;site&nbsp;from&nbsp;the&nbsp;parameter&nbsp;into&nbsp;the&nbsp;_site<br>
instance&nbsp;variable.&nbsp;This&nbsp;is&nbsp;a&nbsp;play&nbsp;on&nbsp;the&nbsp;decorator&nbsp;pattern.<br>
&nbsp;<br>
Argument(s):<br>
site&nbsp;--&nbsp;the&nbsp;site&nbsp;that&nbsp;we&nbsp;will&nbsp;decorate.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-getContentList"><strong>getContentList</strong></a>(self, webcontent)</dt><dd><tt>Retrieves&nbsp;a&nbsp;list&nbsp;of&nbsp;information&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;sites&nbsp;defined<br>
in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;list&nbsp;of&nbsp;found&nbsp;information&nbsp;from&nbsp;the&nbsp;sites&nbsp;being&nbsp;used<br>
as&nbsp;resources&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;site&nbsp;cannot&nbsp;be&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
webcontent&nbsp;--&nbsp;actual&nbsp;content&nbsp;of&nbsp;the&nbsp;web&nbsp;page&nbsp;that's&nbsp;been&nbsp;returned<br>
from&nbsp;a&nbsp;request.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;information&nbsp;found&nbsp;from&nbsp;a&nbsp;web&nbsp;site&nbsp;being&nbsp;used&nbsp;as&nbsp;a&nbsp;resource.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="SingleResultsSite-addResults"><strong>addResults</strong></a>(self, results)</dt><dd><tt>Assigns&nbsp;the&nbsp;argument&nbsp;to&nbsp;the&nbsp;_results&nbsp;instance&nbsp;variable&nbsp;to&nbsp;build<br>
the&nbsp;list&nbsp;or&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.&nbsp;Assign&nbsp;None&nbsp;to&nbsp;the<br>
_results&nbsp;instance&nbsp;variable&nbsp;if&nbsp;the&nbsp;argument&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
results&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-getFullURL"><strong>getFullURL</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;FullURL&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-getImportantProperty"><strong>getImportantProperty</strong></a>(self, index)</dt><dd><tt>Gets&nbsp;the&nbsp;property&nbsp;information&nbsp;from&nbsp;the&nbsp;property&nbsp;value&nbsp;listed&nbsp;in&nbsp;the<br>
sites.xml&nbsp;file&nbsp;for&nbsp;that&nbsp;specific&nbsp;site&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;xml&nbsp;tag.<br>
This&nbsp;Method&nbsp;allows&nbsp;for&nbsp;the&nbsp;property&nbsp;that&nbsp;will&nbsp;be&nbsp;printed&nbsp;to&nbsp;be&nbsp;changed<br>
using&nbsp;the&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;return&nbsp;value&nbsp;listed&nbsp;in&nbsp;the&nbsp;property&nbsp;attribute&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
index&nbsp;--&nbsp;integer&nbsp;representing&nbsp;which&nbsp;important&nbsp;property&nbsp;is&nbsp;retrieved&nbsp;if<br>
more&nbsp;than&nbsp;one&nbsp;important&nbsp;property&nbsp;value&nbsp;is&nbsp;listed&nbsp;in&nbsp;the&nbsp;config&nbsp;file.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Multiple&nbsp;options&nbsp;--&nbsp;returns&nbsp;the&nbsp;return&nbsp;value&nbsp;of&nbsp;the&nbsp;property&nbsp;listed&nbsp;in<br>
the&nbsp;config&nbsp;file.&nbsp;Most&nbsp;likely&nbsp;a&nbsp;string&nbsp;or&nbsp;a&nbsp;list.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-getResults"><strong>getResults</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Results&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-getTarget"><strong>getTarget</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Target&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-getWebScrape"><strong>getWebScrape</strong></a>(self)</dt><dd><tt>Attempts&nbsp;to&nbsp;retrieve&nbsp;a&nbsp;string&nbsp;from&nbsp;a&nbsp;web&nbsp;site.&nbsp;String&nbsp;retrieved&nbsp;is<br>
the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;HTML&nbsp;markup.&nbsp;Requests&nbsp;via&nbsp;proxy&nbsp;if<br>
--proxy&nbsp;option&nbsp;was&nbsp;chosen&nbsp;during&nbsp;execution&nbsp;of&nbsp;the&nbsp;Automater.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;the<br>
HTML&nbsp;markup&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-postMessage"><strong>postMessage</strong></a>(self, message)</dt><dd><tt>Prints&nbsp;multiple&nbsp;messages&nbsp;to&nbsp;inform&nbsp;the&nbsp;user&nbsp;of&nbsp;progress.&nbsp;Assignes<br>
the&nbsp;_messagetopost&nbsp;instance&nbsp;variable&nbsp;to&nbsp;the&nbsp;message.&nbsp;Uses&nbsp;the<br>
MessageToPost&nbsp;property.<br>
&nbsp;<br>
Argument(s):<br>
message&nbsp;--&nbsp;string&nbsp;to&nbsp;be&nbsp;utilized&nbsp;as&nbsp;a&nbsp;message&nbsp;to&nbsp;post.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Class methods inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><a name="SingleResultsSite-buildDictionaryFromXML"><strong>buildDictionaryFromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;dictionary<br>
from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config&nbsp;file.<br>
Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;dictionary&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
Dictionary&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-buildSiteFromXML"><strong>buildSiteFromXML</strong></a>(self, siteelement, webretrievedelay, proxy, targettype, target, useragent)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Utilizes&nbsp;the&nbsp;Class&nbsp;Methods&nbsp;within&nbsp;this&nbsp;Class&nbsp;to&nbsp;build&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
Returns&nbsp;a&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;defines&nbsp;results&nbsp;returned&nbsp;during&nbsp;the&nbsp;web<br>
retrieval&nbsp;investigations.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
webretrievedelay&nbsp;--&nbsp;the&nbsp;amount&nbsp;of&nbsp;seconds&nbsp;to&nbsp;wait&nbsp;between&nbsp;site&nbsp;retrieve<br>
calls.&nbsp;Default&nbsp;delay&nbsp;is&nbsp;2&nbsp;seconds.<br>
proxy&nbsp;--&nbsp;sets&nbsp;a&nbsp;proxy&nbsp;to&nbsp;use&nbsp;in&nbsp;the&nbsp;form&nbsp;of&nbsp;proxy.example.com:8080.<br>
targettype&nbsp;--&nbsp;the&nbsp;targettype&nbsp;as&nbsp;defined.&nbsp;Either&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
target&nbsp;--&nbsp;the&nbsp;target&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;to&nbsp;gather&nbsp;information&nbsp;on.<br>
useragent&nbsp;--&nbsp;the&nbsp;string&nbsp;utilized&nbsp;to&nbsp;represent&nbsp;the&nbsp;user-agent&nbsp;when<br>
web&nbsp;requests&nbsp;or&nbsp;submissions&nbsp;are&nbsp;made.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="SingleResultsSite-buildStringOrListfromXML"><strong>buildStringOrListfromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;string<br>
or&nbsp;list&nbsp;from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config<br>
file.&nbsp;Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;list&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found&nbsp;or&nbsp;a&nbsp;string&nbsp;of&nbsp;that&nbsp;entry&nbsp;if&nbsp;only<br>
one&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;is&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
List&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
string&nbsp;representing&nbsp;an&nbsp;entry&nbsp;key&nbsp;if&nbsp;only&nbsp;one&nbsp;is&nbsp;found<br>
within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<hr>
Data descriptors inherited from <a href="siteinfo.html#Site">Site</a>:<br>
<dl><dt><strong>APIKey</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;an&nbsp;APIKey&nbsp;was&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;APIKey&nbsp;using&nbsp;the<br>
_apikey&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;APIKey&nbsp;from&nbsp;the&nbsp;_apikey<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ErrorMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Error&nbsp;Message.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;error&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FriendlyName</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;friendly&nbsp;string&nbsp;name.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;friendly&nbsp;name&nbsp;for&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FullURL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Headers</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;Headers&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Headers&nbsp;using&nbsp;the<br>
_headers&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Headers&nbsp;from&nbsp;the&nbsp;_headers<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ImportantPropertyString</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Important&nbsp;Property<br>
that&nbsp;the&nbsp;user&nbsp;wants&nbsp;the&nbsp;site&nbsp;to&nbsp;report.&nbsp;This&nbsp;is&nbsp;set&nbsp;using<br>
the&nbsp;sites.xml&nbsp;config&nbsp;file&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;XML&nbsp;tag.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;important&nbsp;property&nbsp;of&nbsp;the&nbsp;site<br>
that&nbsp;needs&nbsp;to&nbsp;be&nbsp;reported.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>MessageToPost</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;the&nbsp;user.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Params</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;web&nbsp;Parameters&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Parameters&nbsp;using&nbsp;the<br>
_params&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Parameters&nbsp;from&nbsp;the&nbsp;_params<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Proxy</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>RegEx</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;regular&nbsp;expression<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;regex&nbsp;used&nbsp;to&nbsp;find&nbsp;info&nbsp;on&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ReportStringForResult</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;report&nbsp;string&nbsp;tag&nbsp;that<br>
precedes&nbsp;reporting&nbsp;information&nbsp;so&nbsp;the&nbsp;user&nbsp;knows&nbsp;what<br>
specifics&nbsp;are&nbsp;being&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting&nbsp;information.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Results</strong></dt>
<dd><tt>Checks&nbsp;the&nbsp;instance&nbsp;variable&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
Returns&nbsp;_results&nbsp;(the&nbsp;results&nbsp;list)&nbsp;or&nbsp;None&nbsp;if&nbsp;it&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;discovered&nbsp;from&nbsp;the&nbsp;site&nbsp;being&nbsp;investigated.<br>
None&nbsp;--&nbsp;if&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Target</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;target&nbsp;being&nbsp;investigated.<br>
The&nbsp;string&nbsp;may&nbsp;be&nbsp;an&nbsp;IP&nbsp;Address,&nbsp;MD5&nbsp;hash,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Target&nbsp;from&nbsp;the&nbsp;_target<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>TargetType</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;target&nbsp;type&nbsp;information&nbsp;whether&nbsp;that&nbsp;be&nbsp;ip,<br>
md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;defined&nbsp;as&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>URL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Domain&nbsp;URL&nbsp;which&nbsp;is<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;URL&nbsp;of&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserAgent</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;user-agent&nbsp;that&nbsp;will<br>
be&nbsp;used&nbsp;when&nbsp;requesting&nbsp;or&nbsp;submitting&nbsp;information&nbsp;to<br>
a&nbsp;web&nbsp;site.&nbsp;This&nbsp;is&nbsp;a&nbsp;user-provided&nbsp;string&nbsp;implemented<br>
on&nbsp;the&nbsp;command&nbsp;line&nbsp;at&nbsp;execution&nbsp;or&nbsp;provided&nbsp;by&nbsp;default<br>
if&nbsp;not&nbsp;added&nbsp;during&nbsp;execution.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;UserAgent&nbsp;from&nbsp;the&nbsp;_userAgent<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>WebRetrieveDelay</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;number&nbsp;of<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;delayed&nbsp;between&nbsp;site&nbsp;retrievals.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;an&nbsp;integer&nbsp;that&nbsp;is&nbsp;the&nbsp;delay&nbsp;in<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;between&nbsp;each&nbsp;web&nbsp;site&nbsp;retrieval.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="Site">class <strong>Site</strong></a>(<a href="__builtin__.html#object">__builtin__.object</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#Site">Site</a>&nbsp;is&nbsp;the&nbsp;parent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;represents&nbsp;each&nbsp;site&nbsp;used<br>
for&nbsp;retrieving&nbsp;information.&nbsp;<a href="#Site">Site</a>&nbsp;stores&nbsp;the&nbsp;results<br>
discovered&nbsp;from&nbsp;each&nbsp;web&nbsp;site&nbsp;discovered&nbsp;when&nbsp;running&nbsp;Automater.<br>
<a href="#Site">Site</a>&nbsp;is&nbsp;the&nbsp;parent&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;to&nbsp;<a href="#SingleResultsSite">SingleResultsSite</a>,&nbsp;<a href="#MultiResultsSite">MultiResultsSite</a>,<br>
<a href="#PostTransactionPositiveCapableSite">PostTransactionPositiveCapableSite</a>,&nbsp;and&nbsp;<a href="#PostTransactionAPIKeySite">PostTransactionAPIKeySite</a>.<br>
&nbsp;<br>
Public&nbsp;Method(s):<br>
(Class&nbsp;Method)&nbsp;buildSiteFromXML<br>
(Class&nbsp;Method)&nbsp;buildStringOrListfromXML<br>
(Class&nbsp;Method)&nbsp;buildDictionaryFromXML<br>
(Property)&nbsp;WebRetrieveDelay<br>
(Property)&nbsp;TargetType<br>
(Property)&nbsp;ReportStringForResult<br>
(Property)&nbsp;FriendlyName<br>
(Property)&nbsp;RegEx<br>
(Property)&nbsp;URL<br>
(Property)&nbsp;MessageToPost<br>
(Property)&nbsp;ErrorMessage<br>
(Property)&nbsp;UserMessage<br>
(Property)&nbsp;FullURL<br>
(Setter)&nbsp;FullURL<br>
(Property)&nbsp;ImportantPropertyString<br>
(Property)&nbsp;Params<br>
(Setter)&nbsp;Params<br>
(Property)&nbsp;Headers<br>
(Property)&nbsp;APIKey<br>
(Property)&nbsp;Target<br>
(Property)&nbsp;UserAgent<br>
(Property)&nbsp;Results<br>
addResults<br>
postMessage<br>
getImportantProperty<br>
getTarget<br>
getResults<br>
getFullURL<br>
getWebScrape<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
_sites<br>
_sourceurl<br>
_webretrievedelay<br>
_targetType<br>
_reportstringforresult<br>
_errormessage<br>
_usermessage<br>
_target<br>
_userAgent<br>
_friendlyName<br>
_regex<br>
_fullURL<br>
_importantProperty<br>
_params<br>
_headers<br>
_apikey<br>
_results<br>
_messagetopost<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%">Methods defined here:<br>
<dl><dt><a name="Site-__init__"><strong>__init__</strong></a>(self, domainurl, webretrievedelay, proxy, targettype, reportstringforresult, target, useragent, friendlyname, regex, fullurl, importantproperty, params, headers, apikey)</dt><dd><tt>Class&nbsp;constructor.&nbsp;Sets&nbsp;the&nbsp;instance&nbsp;variables&nbsp;based&nbsp;on&nbsp;input&nbsp;from<br>
the&nbsp;arguments&nbsp;supplied&nbsp;when&nbsp;Automater&nbsp;is&nbsp;run&nbsp;and&nbsp;what&nbsp;the&nbsp;sites.xml<br>
config&nbsp;file&nbsp;stores.<br>
&nbsp;<br>
Argument(s):<br>
domainurl&nbsp;--&nbsp;string&nbsp;defined&nbsp;in&nbsp;sites.xml&nbsp;in&nbsp;the&nbsp;domainurl&nbsp;XML&nbsp;tag.<br>
webretrievedelay&nbsp;--&nbsp;the&nbsp;amount&nbsp;of&nbsp;seconds&nbsp;to&nbsp;wait&nbsp;between&nbsp;site&nbsp;retrieve<br>
calls.&nbsp;Default&nbsp;delay&nbsp;is&nbsp;2&nbsp;seconds.<br>
proxy&nbsp;--&nbsp;will&nbsp;set&nbsp;a&nbsp;proxy&nbsp;to&nbsp;use&nbsp;(eg.&nbsp;proxy.example.com:8080).<br>
targettype&nbsp;--&nbsp;the&nbsp;targettype&nbsp;as&nbsp;defined.&nbsp;Either&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
reportstringforresult&nbsp;--&nbsp;string&nbsp;or&nbsp;list&nbsp;of&nbsp;strings&nbsp;that&nbsp;are&nbsp;entered&nbsp;in<br>
the&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;within&nbsp;the&nbsp;reportstringforresult&nbsp;XML&nbsp;tag&nbsp;in&nbsp;the<br>
sites.xml&nbsp;configuration&nbsp;file.<br>
target&nbsp;--&nbsp;the&nbsp;target&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;to&nbsp;gather&nbsp;information&nbsp;on.<br>
useragent&nbsp;--&nbsp;the&nbsp;user-agent&nbsp;string&nbsp;that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;when&nbsp;submitting<br>
information&nbsp;to&nbsp;or&nbsp;requesting&nbsp;information&nbsp;from&nbsp;a&nbsp;website<br>
friendlyname&nbsp;--&nbsp;string&nbsp;or&nbsp;list&nbsp;of&nbsp;strings&nbsp;that&nbsp;are&nbsp;entered&nbsp;in<br>
the&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;within&nbsp;the&nbsp;sitefriendlyname&nbsp;XML&nbsp;tag&nbsp;in&nbsp;the<br>
sites.xml&nbsp;configuration&nbsp;file.<br>
regex&nbsp;--&nbsp;the&nbsp;regexs&nbsp;defined&nbsp;in&nbsp;the&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;within&nbsp;the<br>
regex&nbsp;XML&nbsp;tag&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
fullurl&nbsp;--&nbsp;string&nbsp;representation&nbsp;of&nbsp;fullurl&nbsp;pulled&nbsp;from&nbsp;the<br>
sites.xml&nbsp;file&nbsp;in&nbsp;the&nbsp;fullurl&nbsp;XML&nbsp;tag.<br>
importantproperty&nbsp;--&nbsp;string&nbsp;defined&nbsp;in&nbsp;the&nbsp;the&nbsp;sites.xml&nbsp;config&nbsp;file<br>
in&nbsp;the&nbsp;importantproperty&nbsp;XML&nbsp;tag.<br>
params&nbsp;--&nbsp;string&nbsp;or&nbsp;list&nbsp;provided&nbsp;in&nbsp;the&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;within&nbsp;the&nbsp;params<br>
XML&nbsp;tag&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
headers&nbsp;--&nbsp;string&nbsp;or&nbsp;list&nbsp;provided&nbsp;in&nbsp;the&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;within&nbsp;the&nbsp;headers<br>
XML&nbsp;tag&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
apikey&nbsp;--&nbsp;string&nbsp;or&nbsp;list&nbsp;of&nbsp;strings&nbsp;found&nbsp;in&nbsp;the&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;within<br>
the&nbsp;apikey&nbsp;XML&nbsp;tag&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.</tt></dd></dl>

<dl><dt><a name="Site-addResults"><strong>addResults</strong></a>(self, results)</dt><dd><tt>Assigns&nbsp;the&nbsp;argument&nbsp;to&nbsp;the&nbsp;_results&nbsp;instance&nbsp;variable&nbsp;to&nbsp;build<br>
the&nbsp;list&nbsp;or&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.&nbsp;Assign&nbsp;None&nbsp;to&nbsp;the<br>
_results&nbsp;instance&nbsp;variable&nbsp;if&nbsp;the&nbsp;argument&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
results&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="Site-getFullURL"><strong>getFullURL</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;FullURL&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="Site-getImportantProperty"><strong>getImportantProperty</strong></a>(self, index)</dt><dd><tt>Gets&nbsp;the&nbsp;property&nbsp;information&nbsp;from&nbsp;the&nbsp;property&nbsp;value&nbsp;listed&nbsp;in&nbsp;the<br>
sites.xml&nbsp;file&nbsp;for&nbsp;that&nbsp;specific&nbsp;site&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;xml&nbsp;tag.<br>
This&nbsp;Method&nbsp;allows&nbsp;for&nbsp;the&nbsp;property&nbsp;that&nbsp;will&nbsp;be&nbsp;printed&nbsp;to&nbsp;be&nbsp;changed<br>
using&nbsp;the&nbsp;configuration&nbsp;file.<br>
Returns&nbsp;the&nbsp;return&nbsp;value&nbsp;listed&nbsp;in&nbsp;the&nbsp;property&nbsp;attribute&nbsp;discovered.<br>
&nbsp;<br>
Argument(s):<br>
index&nbsp;--&nbsp;integer&nbsp;representing&nbsp;which&nbsp;important&nbsp;property&nbsp;is&nbsp;retrieved&nbsp;if<br>
more&nbsp;than&nbsp;one&nbsp;important&nbsp;property&nbsp;value&nbsp;is&nbsp;listed&nbsp;in&nbsp;the&nbsp;config&nbsp;file.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Multiple&nbsp;options&nbsp;--&nbsp;returns&nbsp;the&nbsp;return&nbsp;value&nbsp;of&nbsp;the&nbsp;property&nbsp;listed&nbsp;in<br>
the&nbsp;config&nbsp;file.&nbsp;Most&nbsp;likely&nbsp;a&nbsp;string&nbsp;or&nbsp;a&nbsp;list.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="Site-getResults"><strong>getResults</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Results&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="Site-getTarget"><strong>getTarget</strong></a>(self)</dt><dd><tt>Returns&nbsp;the&nbsp;Target&nbsp;property&nbsp;information.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="Site-getWebScrape"><strong>getWebScrape</strong></a>(self)</dt><dd><tt>Attempts&nbsp;to&nbsp;retrieve&nbsp;a&nbsp;string&nbsp;from&nbsp;a&nbsp;web&nbsp;site.&nbsp;String&nbsp;retrieved&nbsp;is<br>
the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;HTML&nbsp;markup.&nbsp;Requests&nbsp;via&nbsp;proxy&nbsp;if<br>
--proxy&nbsp;option&nbsp;was&nbsp;chosen&nbsp;during&nbsp;execution&nbsp;of&nbsp;the&nbsp;Automater.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;entire&nbsp;web&nbsp;site&nbsp;including&nbsp;the<br>
HTML&nbsp;markup&nbsp;retrieved&nbsp;from&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="Site-postMessage"><strong>postMessage</strong></a>(self, message)</dt><dd><tt>Prints&nbsp;multiple&nbsp;messages&nbsp;to&nbsp;inform&nbsp;the&nbsp;user&nbsp;of&nbsp;progress.&nbsp;Assignes<br>
the&nbsp;_messagetopost&nbsp;instance&nbsp;variable&nbsp;to&nbsp;the&nbsp;message.&nbsp;Uses&nbsp;the<br>
MessageToPost&nbsp;property.<br>
&nbsp;<br>
Argument(s):<br>
message&nbsp;--&nbsp;string&nbsp;to&nbsp;be&nbsp;utilized&nbsp;as&nbsp;a&nbsp;message&nbsp;to&nbsp;post.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Class methods defined here:<br>
<dl><dt><a name="Site-buildDictionaryFromXML"><strong>buildDictionaryFromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;dictionary<br>
from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config&nbsp;file.<br>
Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;dictionary&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
Dictionary&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="Site-buildSiteFromXML"><strong>buildSiteFromXML</strong></a>(self, siteelement, webretrievedelay, proxy, targettype, target, useragent)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Utilizes&nbsp;the&nbsp;Class&nbsp;Methods&nbsp;within&nbsp;this&nbsp;Class&nbsp;to&nbsp;build&nbsp;the&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
Returns&nbsp;a&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;defines&nbsp;results&nbsp;returned&nbsp;during&nbsp;the&nbsp;web<br>
retrieval&nbsp;investigations.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
webretrievedelay&nbsp;--&nbsp;the&nbsp;amount&nbsp;of&nbsp;seconds&nbsp;to&nbsp;wait&nbsp;between&nbsp;site&nbsp;retrieve<br>
calls.&nbsp;Default&nbsp;delay&nbsp;is&nbsp;2&nbsp;seconds.<br>
proxy&nbsp;--&nbsp;sets&nbsp;a&nbsp;proxy&nbsp;to&nbsp;use&nbsp;in&nbsp;the&nbsp;form&nbsp;of&nbsp;proxy.example.com:8080.<br>
targettype&nbsp;--&nbsp;the&nbsp;targettype&nbsp;as&nbsp;defined.&nbsp;Either&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
target&nbsp;--&nbsp;the&nbsp;target&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;to&nbsp;gather&nbsp;information&nbsp;on.<br>
useragent&nbsp;--&nbsp;the&nbsp;string&nbsp;utilized&nbsp;to&nbsp;represent&nbsp;the&nbsp;user-agent&nbsp;when<br>
web&nbsp;requests&nbsp;or&nbsp;submissions&nbsp;are&nbsp;made.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="Site-buildStringOrListfromXML"><strong>buildStringOrListfromXML</strong></a>(self, siteelement, elementstring)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Takes&nbsp;in&nbsp;a&nbsp;siteelement&nbsp;and&nbsp;then&nbsp;elementstring&nbsp;and&nbsp;builds&nbsp;a&nbsp;string<br>
or&nbsp;list&nbsp;from&nbsp;multiple&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;config<br>
file.&nbsp;Returns&nbsp;None&nbsp;if&nbsp;there&nbsp;are&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;for&nbsp;this<br>
specific&nbsp;elementstring.&nbsp;Returns&nbsp;a&nbsp;list&nbsp;of&nbsp;those&nbsp;entries<br>
if&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found&nbsp;or&nbsp;a&nbsp;string&nbsp;of&nbsp;that&nbsp;entry&nbsp;if&nbsp;only<br>
one&nbsp;entry&nbsp;XML&nbsp;tag&nbsp;is&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
siteelement&nbsp;--&nbsp;the&nbsp;siteelement&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;as&nbsp;the<br>
start&nbsp;element.<br>
elementstring&nbsp;--&nbsp;the&nbsp;string&nbsp;representation&nbsp;within&nbsp;the&nbsp;siteelement<br>
that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;to&nbsp;get&nbsp;to&nbsp;the&nbsp;single&nbsp;or&nbsp;multiple&nbsp;entry<br>
XML&nbsp;tags.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
None&nbsp;if&nbsp;no&nbsp;entry&nbsp;XML&nbsp;tags&nbsp;are&nbsp;found.<br>
List&nbsp;representing&nbsp;all&nbsp;entry&nbsp;keys&nbsp;found&nbsp;within&nbsp;the&nbsp;elementstring.<br>
string&nbsp;representing&nbsp;an&nbsp;entry&nbsp;key&nbsp;if&nbsp;only&nbsp;one&nbsp;is&nbsp;found<br>
within&nbsp;the&nbsp;elementstring.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<hr>
Data descriptors defined here:<br>
<dl><dt><strong>APIKey</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;an&nbsp;APIKey&nbsp;was&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;APIKey&nbsp;using&nbsp;the<br>
_apikey&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;APIKey&nbsp;from&nbsp;the&nbsp;_apikey<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ErrorMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Error&nbsp;Message.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;error&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FriendlyName</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;friendly&nbsp;string&nbsp;name.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;friendly&nbsp;name&nbsp;for&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>FullURL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Headers</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;Headers&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Headers&nbsp;using&nbsp;the<br>
_headers&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Headers&nbsp;from&nbsp;the&nbsp;_headers<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ImportantPropertyString</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Important&nbsp;Property<br>
that&nbsp;the&nbsp;user&nbsp;wants&nbsp;the&nbsp;site&nbsp;to&nbsp;report.&nbsp;This&nbsp;is&nbsp;set&nbsp;using<br>
the&nbsp;sites.xml&nbsp;config&nbsp;file&nbsp;in&nbsp;the&nbsp;importantproperty&nbsp;XML&nbsp;tag.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;important&nbsp;property&nbsp;of&nbsp;the&nbsp;site<br>
that&nbsp;needs&nbsp;to&nbsp;be&nbsp;reported.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>MessageToPost</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;the&nbsp;user.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;message&nbsp;to&nbsp;print&nbsp;to<br>
the&nbsp;standard&nbsp;output.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Params</strong></dt>
<dd><tt>Determines&nbsp;if&nbsp;web&nbsp;Parameters&nbsp;were&nbsp;set&nbsp;for&nbsp;this&nbsp;specific&nbsp;site.<br>
Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Parameters&nbsp;using&nbsp;the<br>
_params&nbsp;instance&nbsp;variable&nbsp;or&nbsp;returns&nbsp;None&nbsp;if&nbsp;the&nbsp;instance<br>
variable&nbsp;is&nbsp;empty&nbsp;or&nbsp;not&nbsp;set.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Parameters&nbsp;from&nbsp;the&nbsp;_params<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Proxy</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;proxy&nbsp;used<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>RegEx</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;regular&nbsp;expression<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;regex&nbsp;used&nbsp;to&nbsp;find&nbsp;info&nbsp;on&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>ReportStringForResult</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;a&nbsp;report&nbsp;string&nbsp;tag&nbsp;that<br>
precedes&nbsp;reporting&nbsp;information&nbsp;so&nbsp;the&nbsp;user&nbsp;knows&nbsp;what<br>
specifics&nbsp;are&nbsp;being&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;a&nbsp;tag&nbsp;for&nbsp;reporting&nbsp;information.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Results</strong></dt>
<dd><tt>Checks&nbsp;the&nbsp;instance&nbsp;variable&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
Returns&nbsp;_results&nbsp;(the&nbsp;results&nbsp;list)&nbsp;or&nbsp;None&nbsp;if&nbsp;it&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;list&nbsp;of&nbsp;results&nbsp;discovered&nbsp;from&nbsp;the&nbsp;site&nbsp;being&nbsp;investigated.<br>
None&nbsp;--&nbsp;if&nbsp;_results&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>Target</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;target&nbsp;being&nbsp;investigated.<br>
The&nbsp;string&nbsp;may&nbsp;be&nbsp;an&nbsp;IP&nbsp;Address,&nbsp;MD5&nbsp;hash,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;Target&nbsp;from&nbsp;the&nbsp;_target<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>TargetType</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;target&nbsp;type&nbsp;information&nbsp;whether&nbsp;that&nbsp;be&nbsp;ip,<br>
md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;defined&nbsp;as&nbsp;ip,&nbsp;md5,&nbsp;or&nbsp;hostname.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>URL</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Domain&nbsp;URL&nbsp;which&nbsp;is<br>
required&nbsp;to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;URL&nbsp;of&nbsp;the&nbsp;site.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserAgent</strong></dt>
<dd><tt>Returns&nbsp;string&nbsp;representing&nbsp;the&nbsp;user-agent&nbsp;that&nbsp;will<br>
be&nbsp;used&nbsp;when&nbsp;requesting&nbsp;or&nbsp;submitting&nbsp;information&nbsp;to<br>
a&nbsp;web&nbsp;site.&nbsp;This&nbsp;is&nbsp;a&nbsp;user-provided&nbsp;string&nbsp;implemented<br>
on&nbsp;the&nbsp;command&nbsp;line&nbsp;at&nbsp;execution&nbsp;or&nbsp;provided&nbsp;by&nbsp;default<br>
if&nbsp;not&nbsp;added&nbsp;during&nbsp;execution.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;the&nbsp;UserAgent&nbsp;from&nbsp;the&nbsp;_userAgent<br>
instance&nbsp;variable.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>UserMessage</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representing&nbsp;the&nbsp;Full&nbsp;URL&nbsp;which&nbsp;is&nbsp;the<br>
domain&nbsp;URL&nbsp;plus&nbsp;querystrings&nbsp;and&nbsp;other&nbsp;information&nbsp;required<br>
to&nbsp;retrieve&nbsp;the&nbsp;information&nbsp;being&nbsp;investigated.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representing&nbsp;the&nbsp;full&nbsp;URL&nbsp;of&nbsp;the&nbsp;site&nbsp;including<br>
querystring&nbsp;information&nbsp;and&nbsp;any&nbsp;other&nbsp;info&nbsp;required.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>WebRetrieveDelay</strong></dt>
<dd><tt>Returns&nbsp;the&nbsp;string&nbsp;representation&nbsp;of&nbsp;the&nbsp;number&nbsp;of<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;delayed&nbsp;between&nbsp;site&nbsp;retrievals.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string&nbsp;--&nbsp;representation&nbsp;of&nbsp;an&nbsp;integer&nbsp;that&nbsp;is&nbsp;the&nbsp;delay&nbsp;in<br>
seconds&nbsp;that&nbsp;will&nbsp;be&nbsp;used&nbsp;between&nbsp;each&nbsp;web&nbsp;site&nbsp;retrieval.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table> <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="SiteFacade">class <strong>SiteFacade</strong></a>(<a href="__builtin__.html#object">__builtin__.object</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#SiteFacade">SiteFacade</a>&nbsp;provides&nbsp;a&nbsp;Facade&nbsp;to&nbsp;run&nbsp;the&nbsp;multiple&nbsp;requirements&nbsp;needed<br>
to&nbsp;automate&nbsp;the&nbsp;site&nbsp;retrieval&nbsp;and&nbsp;storage&nbsp;processes.<br>
&nbsp;<br>
Public&nbsp;Method(s):<br>
runSiteAutomation<br>
(Property)&nbsp;Sites<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
_sites<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%">Methods defined here:<br>
<dl><dt><a name="SiteFacade-__init__"><strong>__init__</strong></a>(self)</dt><dd><tt>Class&nbsp;constructor.&nbsp;Simply&nbsp;creates&nbsp;a&nbsp;blank&nbsp;list&nbsp;and&nbsp;assigns&nbsp;it&nbsp;to<br>
instance&nbsp;variable&nbsp;_sites&nbsp;that&nbsp;will&nbsp;be&nbsp;filled&nbsp;with&nbsp;retrieved&nbsp;info<br>
from&nbsp;sites&nbsp;defined&nbsp;in&nbsp;the&nbsp;sites.xml&nbsp;configuration&nbsp;file.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.</tt></dd></dl>

<dl><dt><a name="SiteFacade-identifyTargetType"><strong>identifyTargetType</strong></a>(self, target)</dt><dd><tt>Checks&nbsp;the&nbsp;target&nbsp;information&nbsp;provided&nbsp;to&nbsp;determine&nbsp;if&nbsp;it&nbsp;is&nbsp;a(n)<br>
IP&nbsp;Address&nbsp;in&nbsp;standard;&nbsp;CIDR&nbsp;or&nbsp;dash&nbsp;notation,&nbsp;or&nbsp;an&nbsp;MD5&nbsp;hash,<br>
or&nbsp;a&nbsp;string&nbsp;hostname.<br>
Returns&nbsp;a&nbsp;string&nbsp;md5&nbsp;if&nbsp;MD5&nbsp;hash&nbsp;is&nbsp;identified.&nbsp;Returns&nbsp;the&nbsp;string<br>
ip&nbsp;if&nbsp;any&nbsp;IP&nbsp;Address&nbsp;format&nbsp;is&nbsp;found.&nbsp;Returns&nbsp;the&nbsp;string&nbsp;hostname<br>
if&nbsp;neither&nbsp;of&nbsp;those&nbsp;two&nbsp;are&nbsp;found.<br>
&nbsp;<br>
Argument(s):<br>
target&nbsp;--&nbsp;string&nbsp;representing&nbsp;the&nbsp;target&nbsp;provided&nbsp;as&nbsp;the&nbsp;first<br>
argument&nbsp;to&nbsp;the&nbsp;program&nbsp;when&nbsp;Automater&nbsp;is&nbsp;run.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
string.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<dl><dt><a name="SiteFacade-runSiteAutomation"><strong>runSiteAutomation</strong></a>(self, webretrievedelay, proxy, targetlist, source, postbydefault, useragent)</dt><dd><tt>Builds&nbsp;site&nbsp;objects&nbsp;representative&nbsp;of&nbsp;each&nbsp;site&nbsp;listed&nbsp;in&nbsp;the&nbsp;sites.xml<br>
config&nbsp;file.&nbsp;Appends&nbsp;a&nbsp;<a href="#Site">Site</a>&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;or&nbsp;one&nbsp;of&nbsp;it's&nbsp;subordinate&nbsp;objects<br>
to&nbsp;the&nbsp;_sites&nbsp;instance&nbsp;variable&nbsp;so&nbsp;retrieved&nbsp;information&nbsp;can&nbsp;be&nbsp;used.<br>
Returns&nbsp;nothing.<br>
&nbsp;<br>
Argument(s):<br>
webretrievedelay&nbsp;--&nbsp;The&nbsp;amount&nbsp;of&nbsp;seconds&nbsp;to&nbsp;wait&nbsp;between&nbsp;site&nbsp;retrieve<br>
calls.&nbsp;Default&nbsp;delay&nbsp;is&nbsp;2&nbsp;seconds.<br>
proxy&nbsp;--&nbsp;proxy&nbsp;server&nbsp;address&nbsp;as&nbsp;server:port_number<br>
targetlist&nbsp;--&nbsp;list&nbsp;of&nbsp;strings&nbsp;representing&nbsp;targets&nbsp;to&nbsp;be&nbsp;investigated.<br>
Targets&nbsp;can&nbsp;be&nbsp;IP&nbsp;Addresses,&nbsp;MD5&nbsp;hashes,&nbsp;or&nbsp;hostnames.<br>
source&nbsp;--&nbsp;String&nbsp;representing&nbsp;a&nbsp;specific&nbsp;site&nbsp;that&nbsp;should&nbsp;only&nbsp;be&nbsp;used<br>
for&nbsp;investigation&nbsp;purposes&nbsp;instead&nbsp;of&nbsp;all&nbsp;sites&nbsp;listed&nbsp;in&nbsp;the&nbsp;sites.xml<br>
config&nbsp;file.<br>
postbydefault&nbsp;--&nbsp;Boolean&nbsp;value&nbsp;to&nbsp;tell&nbsp;the&nbsp;program&nbsp;if&nbsp;the&nbsp;user&nbsp;wants<br>
to&nbsp;post&nbsp;data&nbsp;to&nbsp;a&nbsp;site&nbsp;if&nbsp;a&nbsp;post&nbsp;is&nbsp;required.&nbsp;Default&nbsp;is&nbsp;to&nbsp;NOT&nbsp;post.<br>
useragent&nbsp;--&nbsp;String&nbsp;representing&nbsp;user-agent&nbsp;that&nbsp;will&nbsp;be&nbsp;utilized&nbsp;when<br>
requesting&nbsp;or&nbsp;submitting&nbsp;data&nbsp;to&nbsp;or&nbsp;from&nbsp;a&nbsp;web&nbsp;site.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Nothing&nbsp;is&nbsp;returned&nbsp;from&nbsp;this&nbsp;Method.<br>
&nbsp;<br>
Restriction(s):<br>
The&nbsp;Method&nbsp;has&nbsp;no&nbsp;restrictions.</tt></dd></dl>

<hr>
Data descriptors defined here:<br>
<dl><dt><strong>Sites</strong></dt>
<dd><tt>Checks&nbsp;the&nbsp;instance&nbsp;variable&nbsp;_sites&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
Returns&nbsp;_sites&nbsp;(the&nbsp;site&nbsp;list)&nbsp;or&nbsp;None&nbsp;if&nbsp;it&nbsp;is&nbsp;empty.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
list&nbsp;--&nbsp;of&nbsp;Site&nbsp;objects&nbsp;or&nbsp;its&nbsp;subordinates.<br>
None&nbsp;--&nbsp;if&nbsp;_sites&nbsp;is&nbsp;empty&nbsp;or&nbsp;None.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Property.</tt></dd>
</dl>
<dl><dt><strong>__dict__</strong></dt>
<dd><tt>dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
<dl><dt><strong>__weakref__</strong></dt>
<dd><tt>list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</tt></dd>
</dl>
</td></tr></table></td></tr></table>
</body></html>

echo "  ____  __ __  ______   ___   _____ ____  _       ___  ____  ______ ";
echo " /    ||  |  ||      | /   \ / ___/|    \| |     /   \|    ||      |";
echo "|  o  ||  |  ||      ||     (   \_ |  o  ) |    |     ||  | |      |";
echo "|     ||  |  ||_|  |_||  O  |\__  ||   _/| |___ |  O  ||  | |_|  |_|";
echo "|  _  ||  :  |  |  |  |     |/  \ ||  |  |     ||     ||  |   |  |  ";
echo "|  |  ||     |  |  |  |     |\    ||  |  |     ||     ||  |   |  |  ";
echo "|__|__| \__,_|  |__|   \___/  \___||__|  |_____| \___/|____|  |__|  ";
echo "                                                                    ";

function installDebian () {
    sudo apt-get update;
    sudo apt-get -y install git python2.7 python-pip postgresql apache2;
    pip2 install requests psutil;
    installMSF;
}

function installFedora () {
    sudo yum -y install git python-pip;
    pip2 install requests psutil;
    installMSF;
}

function installOSX () {
  xcode-select --install;
  /usr/bin/ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)";
  echo PATH=/usr/local/bin:/usr/local/sbin:$PATH >> ~/.bash_profile;
  source ~/.bash_profile;
  brew tap homebrew/versions;
  brew install nmap;
  brew install homebrew/versions/ruby21;
  gem install bundler;
  brew install postgresql --without-ossp-uuid;
  initdb /usr/local/var/postgres;
  mkdir -p ~/Library/LaunchAgents;
  cp /usr/local/Cellar/postgresql/9.4.4/homebrew.mxcl.postgresql.plist ~/Library/LaunchAgents/;
  launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist;
  createuser msf -P -h localhost;
  createdb -O msf msf -h localhost;
  installOsxMSF;
}

function installOsxMSF () {
  mkdir /usr/local/share;
  cd /usr/local/share/;
  git clone https://github.com/rapid7/metasploit-framework.git;
  cd metasploit-framework;
  for MSF in $(ls msf*); do ln -s /usr/local/share/metasploit-framework/$MSF /usr/local/bin/$MSF;done;
  sudo chmod go+w /etc/profile;
  sudo echo export MSF_DATABASE_CONFIG=/usr/local/share/metasploit-framework/config/database.yml >> /etc/profile;
  bundle install;
  echo "[!!] A DEFAULT CONFIG OF THE FILE 'database.yml' WILL BE USED";
  rm /usr/local/share/metasploit-framework/config/database.yml;
  cat > /usr/local/share/metasploit-framework/config/database.yml << '_EOF'
production:
  adapter: postgresql
  database: msf
  username: msf
  password:
  host: 127.0.0.1
  port: 5432
  pool: 75
  timeout: 5
_EOF
  source /etc/profile;
  source ~/.bash_profile;
}

function installMSF () {
    if [[ ! "$(which msfconsole)" = */* ]]; then
        curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
            chmod 755 msfinstall && \
            ./msfinstall;
        rm msfinstall;
    fi
}

function install () {
    case "$(uname -a)" in
        *Debian*|*Ubuntu*)
            installDebian;
            ;;
        *Fedora*)
            installFedora;
            ;;
        *Darwin*)
            installOSX;
            ;;
        *)
            echo "Unable to detect operating system that is compatible with AutoSploit...";
            ;;
    esac
    echo "";
    echo "Installation Complete";
}

install;

This repository contains the documentation website code and Markdown source files for [docs.github.com](https://docs.github.com).

GitHub's Docs team works on pre-production content in a private repo that regularly syncs with this public repo.

Use the table of contents icon <img src="/contributing/images/table-of-contents.png" width="25" height="25" /> on the top left corner of this document to navigate to a specific section quickly.

## Contributing

We accept different types of contributions, including some that don't require you to write a single line of code. For detailed instructions on how to get started with our project, see "[About contributing to GitHub Docs](https://docs.github.com/en/contributing/collaborating-on-github-docs/about-contributing-to-github-docs)."


### Ways to contribute
On the GitHub Docs site, you can contribute by clicking the **Make a contribution** button at the bottom of the page to open a pull request for quick fixes like typos, updates, or link fixes.

You can also contribute by creating a local environment or opening a Codespace. For more information, see "[Setting up your environment to work on GitHub Docs](https://docs.github.com/en/contributing/setting-up-your-environment-to-work-on-github-docs)."

<img src="./contributing/images/contribution_cta.png" width="400">

For more complex contributions, please open an issue using the most appropriate [issue template](https://github.com/github/docs/issues/new/choose) to describe the changes you'd like to see.

If you're looking for a way to contribute, you can scan through our [help wanted board](https://github.com/github/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22) to find open issues already approved for work. 

### Join us in discussions

We use GitHub Discussions to talk about all sorts of topics related to documentation and this site. For example: if you'd like help troubleshooting a PR, have a great new idea, or want to share something amazing you've learned in our docs, join us in the [discussions](https://github.com/github/docs/discussions).

### And that's it!

If you're having trouble with your GitHub account, contact [Support](https://support.github.com).

That's how you can easily become a member of the GitHub Docs community. :sparkles:

## READMEs

In addition to the README you're reading right now, this repo includes other READMEs that describe the purpose of each subdirectory in more detail:

- [content/README.md](content/README.md)
- [content/graphql/README.md](content/graphql/README.md)
- [content/rest/README.md](content/rest/README.md)
- [contributing/README.md](contributing/README.md)
- [data/README.md](data/README.md)
- [data/reusables/README.md](data/reusables/README.md)
- [data/variables/README.md](data/variables/README.md)
- [src/README.md](src/README.md)

## License

The GitHub product documentation in the assets, content, and data folders are licensed under a [CC-BY license](LICENSE).

All other code in this repository is licensed under the [MIT license](LICENSE-CODE).

When using the GitHub logos, be sure to follow the [GitHub logo guidelines](https://github.com/logos).

## Thanks :purple_heart:

Thanks for all your contributions and efforts towards improving the GitHub documentation. We thank you for being part of our :sparkles: community :sparkles:!
