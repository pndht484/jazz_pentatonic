# 

<!DOCTYPE html>
<html lang="ja">
<head>

 <meta charset="UTF-8">
 <title>practice</title>

 <script type="text/javascript" src="js/bootstrap.js"></script>
  <script type="text/javascript" src="js/bootstrap.min.js"></script>


 <link rel="stylesheet" href="css/bootstrap.min.css">
 <link href="css/bootstrap.css" rel="stylesheet">
 <link href="style111.css" rel="stylesheet">
 <link href="css/plugins.css" rel="stylesheet">
 <link href="css/style2.css" rel="stylesheet">


 <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
 
 <script>
  (function($){
      const slide = $('#carousel');
      slide
        .carousel({
          interval: 2000,
          pause   : false,
          ride    : false
        })
        .on('click', () => {
          // クリックしたら、スライドを停止する
          slide.carousel('pause');
        })
        .on('slide.bs.carousel', (e) => {
          // prev,nextなどのslideメソッドが実行されると実行される
          console.log('change slide from ' + e.from + ' to ' + e.to + '(' + e.direction + ')');
        })
        .on('slid.bs.carousel', (e) => {
          // スライド遷移が完了すると実行される
          const img = $('img', e.relatedTarget);
          console.log('show slide No.' + e.to + '(', img.attr('src') + ')');
        });

      // ボタン（スライド開始）
      $('#start').on('click', () => {
        slide.carousel('cycle');
      });

      // ボタン（スライド停止）
      $('#stop').on('click', () => {
        slide.carousel('pause');
        // slide.carousel('dispose');
      });

      // ボタン（前へ）
      $('#prev').on('click', () => {
        slide.carousel('prev');
      });

      // ボタン（次へ）
      $('#next').on('click', () => {
        slide.carousel('next');
      });

    })(jQuery);
</script>

</head>

<body>
 

<header class="header">
    <div class="content-wrapper header-nav">
        <h1>Portforio</h1>
        <nav>
            <ul>
                <li><a href="#">トップページ</a></li>
                <li><a href="#">会社概要</a></li>
                <li><a href="#">事業内容</a></li>
                <li><a href="#">採用情報</a></li>
                <li><a href="#">お問い合わせ</a></li>
            </ul>
        </nav>
    </div>
  </header>

  <table class="table">
   <tr>
   <td class="table-img" id="sidebar" ><img src="SAX.jpg"></td>

   <td class="table-img">
   <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel" >
    <ol class="carousel-indicators">
      <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
      <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
      <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
    </ol>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img class="d-block w-100 " src="DSC_0811.jpg"  alt="First slide" width="400"  height="700">
          </div>
      <div class="carousel-item">
        <img class="d-block w-100" src="IMG_0030.jpg" alt="Second slide" width="400"  height="700">
          </div>
      <div class="carousel-item">
        <img class="d-block w-100" src="IMG_0260.jpg" alt="Third slide" width="400"  height="700">
         </div>
    </div>
    <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
   </div>
  </td>
</tr>
</table>
 

  
  
 
<p class="sample-text1">クライアント様の商品を広めるお手伝いをさせて頂きます</p>
<p class="sample-text1">レスポンシブサイトにも対応いたします</p>

   <section class="work">
    <div class="content-wrapper">
    　<h2>事業内容</h2>
      <ul>
        <li><a href="#"><figure><img src="app-1.jpg"></figure><h3>タイトル</h3><p>本文が入ります。本文が入ります。本文が入ります。本文が入ります。本文が入ります。</p></a></li>
        <li><a href="#"><figure><img src="app-3.jpg"></figure><h3>タイトル</h3><p>本文が入ります。本文が入ります。本文が入ります。本文が入ります。本文が入ります。本文が入ります。</p></a></li>
        <li><a href="#"><figure><img src="app-4.jpg"></figure><h3>タイトル</h3><p>本文が入ります。本文が入ります。本文が入ります。本文が入ります。</p></a></li>
      </ul>
    </div>
  </section>


  <!--l-footer-->
  <footer class="content-wrapper header-nav">
    <ul>
      <li><a href="#">© Copyright 2020</a></li>
      <li><a href="#">お問い合わせ</a></li>
     </ul>   
  </footer>
  <!-- /l-footer -->
</body>
</html>
