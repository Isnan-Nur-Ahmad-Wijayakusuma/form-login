<!doctype html>
<html lang="en">
<head>
	<!-- Required meta tags -->
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

	<!-- Bootstrap CSS -->
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css" 
	integrity="sha384-GJzZqFGwb1QTTN6wy59ffF1BuGJpLSa9DkKMp0DgiMDm4iYMj70gZWKYbI706tWS" 
	crossorigin="anonymous">

	<title>Test page 1</title>
</head>
<body>
	<div class="container">
	<div class="row">
	<div class="col-md-4 offset-md-4">
		<div class="card mt-5">
		<div class="card-title text-center">
			<h1>OOP CHECK</h1>
		</div>
		<div class="card-body">
		<form action="<?php echo htmlspecialchars($_SERVER['PHP_SELF']);?>" method="POST">
			<div class="form-group">
				<label for="username">Nama produk</label>
				<input type="text" name="Nama" class="form-control" placeholder="product name">
				</div>
			<div class="form-group">
                <label for="genre">Tipe produk</label>
				<input type="text" name="tipe" class="form-control" placeholder="type">
			</div>
			<div class="form-group">
                <label for="genre">Kisaran harga</label>
				<input type="text" name="kisaran" class="form-control" placeholder="type">
			</div>
				<button type="submit" name="submit" class="btn btn-primary">Submit</button>
                <input type="submit" name="array" class="btn btn-primary" value="Transform to array">
			</form>
		</div>
	</div>
	</div>
	</div>
	</div>
    <?php
    //Agar suatu function/method can be use on many class
    interface produktipe {
        public function getTipeOS();
      }
    //Hah?! This syntax FOR WHAT??
    /*Yeah man, this is for Array from user input. And what you know guys?
      Yup, this array will be check machine for input test*/
    function printIterable(iterable $itemPutih)    {
        foreach ($itemPutih as $I) {
            echo $I;
        }
        str_split($I);     
    }
    //PARENT (pewarisan)
    class Produk{
        //PROPERTY
        protected $name;
        private $kisaran;
        public  $jenisProduk;
        public static $OSTipe = "Linux";

        //FUNCT or METHOD or whatever will be best web input constructure
        public function __construct($name,  $jenisProduk ,$kisaran) {       
            $this->name = $name;
            $this->jenisProduk = $jenisProduk;
            $this->kisaran = $kisaran;
        }
        public function getTipeOS(){
            return self::$OSTipe;
        }
        public function infoLengkap(){
            $key = array(self::$OSTipe, $this->name, $this->jenisProduk, $this->kisaran);
            return $key;
        }
        public function intro(){
            echo "Nama: {$this->name} | Type {$this->jenisProduk}<br>Kisaran harga:{$this->kisaran}<br>";
        }
        public function __destruct(){
            echo "Destruct func has been actived";
        }
    }
    //CHILD (pewarisan)
    class laptop extends Produk {
        public function message(){   
            echo "[Laptop] ";
        }
    }
    //LOGIC
  /*Perulangan, if you choose CARI, it will be execute and if not, 
    this PERULANGAN never will be execute*/
    if (isset($_POST['submit'])) {
        $name = $_POST['Nama'];$jenisProduk = $_POST['tipe'];
        $kisaran = $_POST['kisaran'];
        $produk = array($name, $jenisProduk, $kisaran);
        
        //Product OR Object
        $produk1 = new laptop($name, $jenisProduk,$kisaran);
        $produk1->message();
        $produk1->intro();
    }
  /*Perulangan, if you choose array, it will be execute and if not, 
    this PERULANGAN never will be execute*/
    elseif (isset($_POST['array'])) {
        $name = $_POST['Nama'];$jenisProduk = $_POST['tipe'];
        $kisaran = $_POST['kisaran'];

        //Product OR Object
        $produk1 = new laptop($name, $jenisProduk,$kisaran);
        $A = $produk1->infoLengkap();
        print_r($A);
    }
?>
</body>
</html>
