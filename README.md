# GitHub Docs <!-- omid in toc -->
#!/bin/bash

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<html><head><title>Python: module inputs</title>
</head><body bgcolor="#f0f0f8">

<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="heading">
<tr bgcolor="#7799ee">
<td valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial">&nbsp;<br><big><big><strong>inputs</strong></big></big></font></td
><td align=right valign=bottom
><font color="#ffffff" face="helvetica, arial"><a href=".">index</a><br><a href="file:/home/jim/Files/TekDefense/TekDefense-Automater-Private/inputs.py">/home/jim/Files/TekDefense/TekDefense-Automater-Private/inputs.py</a></font></td></tr></table>
    <p><tt>The&nbsp;inputs.py&nbsp;module&nbsp;represents&nbsp;some&nbsp;form&nbsp;of&nbsp;all&nbsp;inputs<br>
to&nbsp;the&nbsp;Automater&nbsp;program&nbsp;to&nbsp;include&nbsp;target&nbsp;files,&nbsp;and<br>
the&nbsp;standard&nbsp;config&nbsp;file&nbsp;-&nbsp;sites.xml.&nbsp;Any&nbsp;addition&nbsp;to<br>
Automater&nbsp;that&nbsp;brings&nbsp;any&nbsp;other&nbsp;input&nbsp;requirement&nbsp;should<br>
be&nbsp;programmed&nbsp;in&nbsp;this&nbsp;module.<br>
&nbsp;<br>
Class(es):<br>
<a href="#TargetFile">TargetFile</a>&nbsp;--&nbsp;Provides&nbsp;a&nbsp;representation&nbsp;of&nbsp;a&nbsp;file&nbsp;containing&nbsp;target<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;strings&nbsp;for&nbsp;Automater&nbsp;to&nbsp;utilize.<br>
<a href="#SitesFile">SitesFile</a>&nbsp;--&nbsp;Provides&nbsp;a&nbsp;representation&nbsp;of&nbsp;the&nbsp;sites.xml<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;configuration&nbsp;file.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>
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
<td width="100%"><table width="100%" summary="list"><tr><td width="25%" valign=top><a href="os.html">os</a><br>
</td><td width="25%" valign=top></td><td width="25%" valign=top></td><td width="25%" valign=top></td></tr></table></td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ee77aa">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Classes</strong></big></font></td></tr>
    
<tr><td bgcolor="#ee77aa"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl>
<dt><font face="helvetica, arial"><a href="__builtin__.html#object">__builtin__.object</a>
</font></dt><dd>
<dl>
<dt><font face="helvetica, arial"><a href="inputs.html#SitesFile">SitesFile</a>
</font></dt><dt><font face="helvetica, arial"><a href="inputs.html#TargetFile">TargetFile</a>
</font></dt></dl>
</dd>
</dl>
 <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="SitesFile">class <strong>SitesFile</strong></a>(<a href="__builtin__.html#object">__builtin__.object</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#SitesFile">SitesFile</a>&nbsp;represents&nbsp;an&nbsp;XML&nbsp;Elementree&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;representing&nbsp;the<br>
program's&nbsp;configuration&nbsp;file.&nbsp;Returns&nbsp;XML&nbsp;Elementree&nbsp;<a href="__builtin__.html#object">object</a>.<br>
&nbsp;<br>
Method(s):<br>
(Class&nbsp;Method)&nbsp;getXMLTree<br>
(Class&nbsp;Method)&nbsp;fileExists<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
No&nbsp;instance&nbsp;variables.<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%">Class methods defined here:<br>
<dl><dt><a name="SitesFile-fileExists"><strong>fileExists</strong></a>(self)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Checks&nbsp;if&nbsp;a&nbsp;file&nbsp;exists.&nbsp;Returns&nbsp;boolean&nbsp;representing&nbsp;if&nbsp;file&nbsp;exists.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Boolean<br>
&nbsp;<br>
Restrictions:<br>
File&nbsp;must&nbsp;be&nbsp;named&nbsp;sites.xml&nbsp;and&nbsp;must&nbsp;be&nbsp;in&nbsp;same&nbsp;directory&nbsp;as&nbsp;caller.<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<dl><dt><a name="SitesFile-getXMLTree"><strong>getXMLTree</strong></a>(self)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Opens&nbsp;a&nbsp;config&nbsp;file&nbsp;for&nbsp;reading.<br>
Returns&nbsp;XML&nbsp;Elementree&nbsp;<a href="__builtin__.html#object">object</a>&nbsp;representing&nbsp;XML&nbsp;Config&nbsp;file.<br>
&nbsp;<br>
Argument(s):<br>
No&nbsp;arguments&nbsp;are&nbsp;required.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
ElementTree<br>
&nbsp;<br>
Restrictions:<br>
File&nbsp;must&nbsp;be&nbsp;named&nbsp;sites.xml&nbsp;and&nbsp;must&nbsp;be&nbsp;in&nbsp;same&nbsp;directory&nbsp;as&nbsp;caller.<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<hr>
Data descriptors defined here:<br>
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
<font color="#000000" face="helvetica, arial"><a name="TargetFile">class <strong>TargetFile</strong></a>(<a href="__builtin__.html#object">__builtin__.object</a>)</font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#TargetFile">TargetFile</a>&nbsp;provides&nbsp;a&nbsp;Class&nbsp;Method&nbsp;to&nbsp;retrieve&nbsp;information&nbsp;from&nbsp;a&nbsp;file-<br>
based&nbsp;target&nbsp;when&nbsp;one&nbsp;is&nbsp;entered&nbsp;as&nbsp;the&nbsp;first&nbsp;parameter&nbsp;to&nbsp;the&nbsp;program.<br>
&nbsp;<br>
Public&nbsp;Method(s):<br>
(Class&nbsp;Method)&nbsp;TargetList<br>
&nbsp;<br>
Instance&nbsp;variable(s):<br>
No&nbsp;instance&nbsp;variables.<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%">Class methods defined here:<br>
<dl><dt><a name="TargetFile-TargetList"><strong>TargetList</strong></a>(self, filename)<font color="#909090"><font face="helvetica, arial"> from <a href="__builtin__.html#type">__builtin__.type</a></font></font></dt><dd><tt>Opens&nbsp;a&nbsp;file&nbsp;for&nbsp;reading.<br>
Returns&nbsp;each&nbsp;string&nbsp;from&nbsp;each&nbsp;line&nbsp;of&nbsp;a&nbsp;single&nbsp;or&nbsp;multi-line&nbsp;file.<br>
&nbsp;<br>
Argument(s):<br>
filename&nbsp;--&nbsp;string&nbsp;based&nbsp;name&nbsp;of&nbsp;the&nbsp;file&nbsp;that&nbsp;will&nbsp;be&nbsp;retrieved&nbsp;and&nbsp;parsed.<br>
&nbsp;<br>
Return&nbsp;value(s):<br>
Iterator&nbsp;of&nbsp;string(s)&nbsp;found&nbsp;in&nbsp;a&nbsp;single&nbsp;or&nbsp;multi-line&nbsp;file.<br>
&nbsp;<br>
Restriction(s):<br>
This&nbsp;Method&nbsp;is&nbsp;tagged&nbsp;as&nbsp;a&nbsp;Class&nbsp;Method</tt></dd></dl>

<hr>
Data descriptors defined here:<br>
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
