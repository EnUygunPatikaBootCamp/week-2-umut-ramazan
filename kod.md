```
<?php
abstract class information
{   
    public $numberPlate;
    public $brand;
    public $model;
    public $wheelNo;
    public $wingspan;

    function __construct($numberPlate,$brand,$model,$wheelNo,$wingspan)
    {   
        $this->numberPlate=$numberPlate;    
        $this->brand=$brand;
        $this->model=$model;
        $this->wheelNo=$wheelNo;
        $this->wingspan=$wingspan;
    }
    
    function share(){}
}

class car extends information
{
    function share()
    {
        echo 'Plaka No: '.$this->numberPlate.'<br>Marka: '.$this->brand.'<br>Model: '.$this->model.'<br>Tekerlek Sayısı: '.$this->wheelNo.'<br>';
    }
}

class motorcycle extends information
{
    function share()
    {
        echo 'Plaka No: '.$this->numberPlate.'<br>Marka: '.$this->brand.'<br>Model: '.$this->model.'<br>Tekerlek Sayısı: '.$this->wheelNo.'<br>';
    }
}

class plane extends information
{
    function share()
    {
        echo 'Marka: '.$this->brand.'Model: '.$this->model.'Kanat Açıklığı: '.$this->wingspan.'<br>';
    }
}
$car = new car('06 ARAC 06','Mercedes','C180','4','');
$car->share();

$motorcycle= new motorcycle('06 ARAC 06','Honda','Forza 750','2','');
$motorcycle->share();


$plane = new plane('','Airbus','A380','','80m');
$plane->share();


```