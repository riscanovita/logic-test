<?php 

    // NOMER 1
    $int = 4; 

    for($i = $int - 1; $i >= 1; $i--) {
        $int *= $i;
    }
    echo $int; 

    echo"<br>";
    echo"==========================================================";
    echo"<br>";


    //NOMER 2
    $input = "abcde";
    $j = strlen($input);   
    
    for ($i = 1; $i <= $j; $i++) {
        $output = $input[-$i];

        echo $output;
    }
    

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    // NOMER 3

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    //NOMER 4
    $a = 3;
    $b = 7;
    [$a, $b] = [$b, $a];
    echo "a = " .$a;
    echo "<br>";
    echo "b = ". $b;

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    //NOMER 5
    function penyebut($nilai)
    {
    $nilai = abs($nilai);
    $huruf = array("", "satu", "dua", "tiga", "empat", "lima", "enam", "tujuh", "delapan", "sembilan", "sepuluh", "sebelas");
    $output = "";
        if ($nilai <= 0 or $nilai > 100) {
            echo "silahkan masukkan bilangan 1-100";
        } else if ($nilai < 12) {
            $output = " " . $huruf[$nilai];
        } else if ($nilai < 20) {
            $output = penyebut($nilai - 10) ." belas";
        } else if ($nilai < 100) {
            $output = penyebut($nilai / 10) ." puluh".penyebut($nilai % 10);
        } else {
            echo "seratus";
        }

        return $output;
    }

    $angka = 15;
    echo penyebut($angka);

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    //NOMER 6
    $array = [1, 4, 7, 9, 12];
    $low = 2;
    $high = 15;
    $result = [];

    foreach ($array as $key => $arr) {
        if ($arr >= $low && $arr<= $high) {
            $result[] = $arr;
        }
    }
    print_r ($result);

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    //NOMER 7
    $array = [1, 4, 7, 9, 12];
    $low = 2;
    $high = 15;
    $result = [];

    foreach ($array as $key => $arr) {
        if ($arr >= $low && $arr<= $high) {
            $result[] = $arr;
        }
    }
    echo count($result);

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    //NOMER 8
    $int = 15;
    for ($i=1; $i <= $int; $i++) { 
        if ($i % 3 == 0 && $i % 5 == 0) {
            echo "EduWork";
        } else if ($i % 3 == 0) {
            echo "Edu";
        } else if ($i % 5 == 0) {
            echo "Work";
        } else {
            echo $i;
        }
        echo "<br>";
    }

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    //NOMER 9
    function nilaiMax($array)  
    { 
    $n = count($array);  
    $max = $array[0]; 
    for ($i = 1; $i < $n; $i++)  
        if ($max < $array[$i]) 
            $max = $array[$i]; 
        return $max;        
    } 

    function nilaiMin($array)  
    { 
    $n = count($array);  
    $min = $array[0]; 
    for ($i = 1; $i < $n; $i++)  
        if ($min > $array[$i]) 
            $min = $array[$i]; 
        return $min;        
    } 
    $array = [4,2,6,88,3,11]; 
    echo "high : ".nilaiMax($array).", "."low : ".nilaiMin($array); 

    echo"<br>";
    echo"==========================================================";
    echo"<br>";

    //NOMER 10
    function Kabisat($thn) {
        if ($thn % 4 == 0) {
            echo "$thn adalah tahun kabisat";
        } 
        else if ($thn % 4 != 0) {
            echo "$thn bukan tahun kabisat";
        }
    }
    echo Kabisat(2024);

?>