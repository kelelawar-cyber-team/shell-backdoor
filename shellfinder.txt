<?php

//Shell Finder Script
//Scan for shells at any site

echo'
<style>
a{
text-decoration:none;
color: #009900;
}
body{
color: #009900;
}
input[type=text] {
    padding: 3px;
    color: #009900;
    text-shadow: #777777 0px 0px 3px;
    border: 1px solid #007700;
    background: transparent;
    box-shadow: 0px 0px 4px #007700;
    padding: 3px;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    -webkit-box-shadow: rgb(85,85,85) 0px 0px 4px;
    -moz-box-shadow: rgb(85,85,85) 0px 0px 4px;
}
input[type=submit]:hover, input[type=text]:hover {
    color: #ffffff;
    text-shadow: #006600 0px 0px 4px;
    box-shadow: 0px 0px 4px #00dd00;
    border: 1px solid #00dd00;
    padding: 3px;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    -webkit-box-shadow: rgba(0,119,0) 0px 0px 4px;
    -moz-box-shadow: rgba(0,119,0) 0px 0px 4px;
}
input[type=submit] {
    padding: 3px;
    color: #00770;
    font-weight: bold;
    text-align: center;
    text-shadow: 0 1px rgba(255, 255, 255, 0.3);
    background: #aeaeae;
    background-clip: padding-box;
    border: 1px solid #284473;
    border-bottom-color: #223b66;
    border-radius: 4px;
    cursor: pointer;
    background-image: -webkit-linear-gradient(top, #eaeaea, #d0d0d0);
    background-image: -moz-linear-gradient(top, #eaeaea, #d0d0d0);
    background-image: -o-linear-gradient(top, #eaeaea, #d0d0d0);
    background-image: linear-gradient(to bottom, #eaeaea, #d0d0d0);
    -webkit-box-shadow: inset 0 1px rgba(255, 255, 255, 0.5), inset 0 0 7px rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.15);
    box-shadow: inset 0 1px rgba(255, 255, 255, 0.5), inset 0 0 7px rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.15);
}
</style>
<body bgcolor=#222222>
<center>
<br><center><span style="font-weight:bold;text-shadow:0px 0px 10px #009900 ;font-size:30px; font-family:Lucida Console; color:#009900">Website Shell Finder</span><br><br>
<img src="http://www11.0zz0.com/2014/08/22/21/592562836.png">
<p align="center"></p><br>
<form method="POST">
</form><center>
<form action="" method="post">
<input name="target" type="text" size="100" value="http://site.org/"/><br>
<br><br>
<input name="scan" size="100" value="Start Scaning" type="submit">
</form><br>';

set_time_limit(0);

if (isset($_POST["scan"])) {  

$url = $_POST['traget'];

echo "<br /><span class='start'>Scanning ".$url."<br /><br /></span>";
echo "Results:<br /><br />";

//Tambahin Lagi bro, Biar Kemungkinan Ketemunya Tinggi, Setinggi Harapan Aku Memiliki Dia > :(
$shells = array("WSO.php","dz.php","cpanel.php","cpn.php","sql.php","mysql.php","madspot.php","cp.php","cpbt.php","sYm.php",
"x.php","r99.php","lol.php","jo.php","wp.php","whmcs.php","shellz.php","d0main.php","d0mains.php","users.php",
"Cgishell.pl","killer.php","changeall.php","2.php","Sh3ll.php","dz0.php","dam.php","user.php","dom.php","whmcs.php",
"vb.zip","r00t.php","c99.php","gaza.php","1.php","wp.zip"."wp-content/plugins/disqus-comment-system/disqus.php",
"d0mains.php","wp-content/plugins/akismet/akismet.php","madspotshell.php","Sym.php","c22.php","c100.php",
"wp-content/plugins/akismet/admin.php#","wp-content/plugins/google-sitemap-generator/sitemap-core.php#",
"wp-content/plugins/akismet/widget.php#","Cpanel.php","zone-h.php","tmp/user.php","tmp/Sym.php","cp.php",
"tmp/madspotshell.php","tmp/root.php","tmp/whmcs.php","tmp/index.php","tmp/2.php","tmp/dz.php","tmp/cpn.php",
"tmp/changeall.php","tmp/Cgishell.pl","tmp/sql.php","tmp/admin.php","cliente/downloads/h4xor.php",
"whmcs/downloads/dz.php","L3b.php","d.php","tmp/d.php","tmp/L3b.php","wp-content/plugins/akismet/admin.php",
"templates/rhuk_milkyway/index.php","templates/beez/index.php","admin1.php","upload.php","up.php","vb.zip","vb.rar",
"admin2.asp","uploads.php","sa.php","sysadmins/","admin1/","administration/Sym.php","images/Sym.php",
"/r57.php","/wp-content/plugins/disqus-comment-system/disqus.php","/shell.php","/sa.php","/admin.php","/b374k.php",
"/sa2.php","/2.php","/gaza.php","/up.php","/upload.php","/uploads.php","/templates/beez/index.php","shell.php","/amad.php",
"/t00.php","/dz.php","/site.rar","/Black.php","/site.tar.gz","/home.zip","/home.rar","/home.tar","/home.tar.gz",
"/forum.zip","/forum.rar","/forum.tar","/forum.tar.gz","/test.txt","/ftp.txt","/user.txt","/site.txt","/error_log","/error",
"/cpanel","/awstats","/site.sql","/vb.sql","/forum.sql","/backup.sql","/back.sql","/data.sql","wp.rar/",
"wp-content/plugins/disqus-comment-system/disqus.php","asp.aspx","/templates/beez/index.php","tmp/vaga.php",
"tmp/killer.php","whmcs.php","tmp/killer.php","tmp/domaine.pl","tmp/domaine.php","useradmin/",
"tmp/d0maine.php","d0maine.php","tmp/sql.php","tmp/dz1.php","dz1.php","forum.zip","Symlink.php","Symlink.pl", 
"forum.rar","joomla.zip","joomla.rar","wp.php","buck.sql","sysadmin.php","images/c99.php", "xd.php", "c100.php",
"spy.aspx","xd.php","tmp/xd.php","sym/root/home/","billing/killer.php","tmp/upload.php","tmp/admin.php",
"Server.php","tmp/uploads.php","tmp/up.php","Server/","wp-admin/c99.php","tmp/priv8.php","priv8.php","cgi.pl/", 
"tmp/cgi.pl","downloads/dom.php","templates/ja-helio-farsi/index.php","webadmin.html","admins.php",
"/wp-content/plugins/count-per-day/js/yc/d00.php", "admins/","admins.asp","admins.php","wp.zip");

//Start Scan
foreach ($shells as $shell){
$headers = get_headers("$url$shell"); // 

if (eregi('200', $headers[0])) {
//Result
echo "<a href='$url$shell'>$url$shell</a> <span class='found'>Done :D</span><br /><br/><br/>"; // 
$dz = fopen('shells.txt', 'a+');
$suck = "$url$shell";
fwrite($dz, $suck."\n");
}
}
//Result In Text File (shells.txt)
echo "Shells Added to  File [ <a href='./shells.txt' target='_blank'>shells.txt</a> ]</span>";
}
echo"</center>";
echo"</body>";
echo"</html>";
?>