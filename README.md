<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <title>Document</title>
</head>
<style>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    body{
        height: 100vh;
        background-color: #FFFFFF;
        background-image: linear-gradient(180deg, #FFFFFF 0%, #6284FF 50%, #FF0000 100%);
        justify-content: center;
        align-items: center;
        display: flex;
    }
  
    .open_modal_button{
        padding: 20px 30px;
        background-color: #FBAB7E;
        background-image: linear-gradient(62deg, #FBAB7E 0%, #F7CE68 100%);
        color: black;
        border: none;
        border-radius: 10px;
        font-size: 16px;
        font-weight: bold;
        font-family: Arial, Helvetica, sans-serif;
    }
    
    .modal{
        position: fixed;
        top: 0;
        height: 100vh;
        width: 100vw;
        font-weight: bold;
        font-family: Arial, Helvetica, sans-serif;
    }
    .modal_inner{
        width: 400px;
        height: 200px;
        top: 10%;
        position: relative;
        margin: auto;
        background: white;
        border-radius: 6px;
        overflow: hidden;
        animation: modalShow 0.3s linear;
    }
    .modal_header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 17px;
        background: rgb(245, 115, 136);
        color: rgb(253, 251, 251);
    }
    .modal_header i{
        padding: 5px 6px;
        border: 2px solid white;
        border-radius: 50%;
        color: white;
    }
    
    .modal_header i:hover{
        border-radius: 50%;
        background-color: #4158D0;
        background-image: linear-gradient(43deg, #4158D0 0%, #C850C0 46%, #FFCC70 100%);
    }

    .modal_body{
        color: rgb(245, 115, 136);
        padding: 15px 5px;
    }
    .modal_footer{
        text-align: right;
        padding: 15px;
    }
    .modal_footer button{
        padding: 10px 20px;
        background: rgb(245, 115, 136);
        color: rgb(253, 252, 252);
        border: none;
        border-radius: 10px;
        font-size: 16px;
        font-weight: bold;
        font-family: Arial, Helvetica, sans-serif;
        outline: none;
        cursor: pointer;
    }
    .modal_footer button:hover{
        background-color: #52ACFF;
        background-color: #4158D0;
        background-image: linear-gradient(43deg, #4158D0 0%, #C850C0 46%, #FFCC70 100%);

    }

    .hide{
        display: none;
    }
    @keyframes modalShow {
    from{
     top: -200px;
     opacity: 0;
    }
     to{
         top: 10%;
         opacity: 1;
     }
 }
</style>
<body>
    <button class="open_modal_button">click me</button>
    
    <div class="modal hide">
        <div class="modal_inner">
            <div class="modal_header">
                <h3>Nguyễn Văn Anh Tú</h3>
                <i class="fa-solid fa-xmark"></i>
            </div>
            <div class="modal_body">
                <h2>Modal</h2>
                <p>Đây là phần body của modal</p>
            </div>
            <div class="modal_footer">
                <button>close</button>
            </div>
        </div>
    </div>
    

    
</body>

<script>
    var btnOpen = document.querySelector('.open_modal_button')
    var modal = document.querySelector('.modal')
    var iconClose = document.querySelector('.modal_header i')
    var btnClose = document.querySelector('.modal_footer button')

    function toggleModal(e) {
        modal.classList.toggle('hide')
    }

    btnOpen.addEventListener('click', toggleModal)
    btnClose.addEventListener('click', toggleModal)
    iconClose.addEventListener('click', toggleModal)
    modal.addEventListener('click', function (e) {
        if (e.target == e.currentTarget) {
            toggleModal()
        }
    })

</script>

</html>
