<template>
    <div id="contact-us" class="contacts">
        <div class="container">
            <div class="row">
                <div class="col-lg-7">
                    <h2>Get In Touch</h2>
                    <div class="form">
                        <form class="row p-0">
                            <div class="col-md-5">
                                <div class="form-group mb-4">
                                    <input class="form-control" id="your_name" name="userName" placeholder="Name" required="" type="text">
                                </div>
                                <div class="form-group mb-4">
                                    <input class="form-control" id="your_email" name="userEmail" placeholder="Email" required="" type="email">
                                </div>
                                <div class="form-group mb-4">
                                    <input class="form-control" id="subject" name="userSubject" placeholder="Subject" required="" type="text">
                                </div>
                            </div>
                            <div class="col-md-7">
                            <div class="form-group">
                                <textarea class="form-control" id="message" name="userMessage" placeholder="Message" rows="8"></textarea>
                            </div>
                        </div>
                            <div class="col-md-12">
                                <button class="my-btn mt-4">Send Message<span></span><span></span><span></span><span></span></button>
                            </div>
                        </form>
                    </div>
                </div>
                <div class="col-lg-5 contact-details">
                    <h2>Our Location</h2>
                    <p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered.</p>
                    <ul class="contacts">
                        <li>
                            <i class="fa-solid fa-location-dot"></i>
                            <p>123 Park Avenue, New York, United States</p>
                        </li>
                        <li>
                            <i class="fa-solid fa-phone-volume"></i>
                            <a href="#">+1 631 1234 5678 </a> <a href="#"> +1 631 1234 5678</a>
                        </li>
                        <li>
                            <i class="fa-solid fa-paper-plane"></i>
                            <a href="#">email@website.com </a> <a href="#"> abc@website.com</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ContactComponent'
}
</script>

<style scoped>

#contact-us {
    padding: 0 0 100px 0;
}

h2 {
    margin-bottom: 35px;
    color: #404854;
    font-weight: 600;
    font-size: 40px;
}

.form-control {
    padding: 12px;
    font-size: 14px;
    color: #696969;
    border: 1px solid #d4d4d4;
}

.form-control:focus {
    box-shadow: none;
    border-color: #d4d4d4;
}

.my-btn {
    --c: #00A8F5;
    color: white;
    background-color: #7004BC;
    border-color: #7004BC;
    margin-top: 30px;
    padding: 10px 30px;
    font-weight: 700;
    width: 100%;
}

.my-btn:hover {
    color: white;
    background-color: transparent;
    border-color: #00A8F5;
}

.contact-details {
    padding: 0 40px;
    background-color: #ffffff;
    background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23dedede' fill-opacity='0.33'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
}

p {
    color: #696969;
    font-size: 16px;
    margin-bottom: 25px;
    display: inline-block;
    font-weight: 300;
}

ul {
    list-style: none;
    padding-left: 0;
}

i {
    background: #3264f5;
    background: -moz-linear-gradient(left, #3264f5 2%, #7004bc 82%);
    background: -webkit-linear-gradient(left, #3264f5 2%, #7004bc 82%);
    background: linear-gradient(to right, #3264f5 2%, #7004bc 82%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 25px;
    margin-right: 20px;
}

a {
    color: #696969;
    font-size: 16px;
    text-decoration: none;
    display: inline-block;
    margin-bottom: 25px;
    margin-right: 10px;
    font-weight: 300;
}

a:hover {
    color: #00A8F5;
}




</style>