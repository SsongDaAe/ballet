      // 버튼 클릭시 전체 메뉴 보이기
      $(".tit .btn").click(function(e){
        e.preventDefault();
        $("#cont-nav").slideToggle();
        $(this).toggleClass("on");
    });

    // slick 라이브러리
    $(".ban").slick({
        infinite: true,
        slidesToShow: 3,
        slidesToScroll: 1,
        autoplay: true,
        autoplaySpeed: 2000,
        dots: true,
    });
    $(".gallery_img").slick({
        arrows: false,
        autoplay: true,
        fade: true,
        autoplaySpeed: 2000,
    });
    $(".play").click(function(){
        $(".gallery_img").slick("slickPlay");
    });
    $(".pause").click(function(){
        $(".gallery_img").slick("slickPause");
    });
    $(".next").click(function(){
        $(".gallery_img").slick("slickNext");
    });
    $(".prev").click(function(){
        $(".gallery_img").slick("slickPrev");
    });


    // 탭메뉴
    var $tab_list = $(".tab_menu");
    var $tab_btn = $tab_list.find(">ul>li");

    $tab_btn.on("click focusin", function(e){
        e.preventDefault();

        var $this = $(this);
        $tab_list.find("ul ul").hide();
        $this.children("ul").show();
        $tab_btn.removeClass("active");
        $this.addClass("active");
    });

    // 레이어팝업
    $(".layer").click(function(e){
        e.preventDefault();
        $("#layer").fadeIn(200);
    });
    $(".close").click(function(e){
        e.preventDefault();
        $("#layer").fadeOut(200);
    });

    // 윈도우팝업
    $(".window").click(function(e){
        e.preventDefault();
        // window.open("파일명", "팝업이름", "옵션설정");
        var options = "width=800, height=590, left=50, top=50, scrollbars=0, toolbar=0, menubar=0";
        window.open("popup.html", "popup01", options);
    })

    // 라이트박스
    $(".lightgallery").lightGallery({
        progressBar: true,
    });