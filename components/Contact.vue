<template>
    <section id="section-contact" class="formulario">
        <div class="container contact">
            <div class="row">
                <h3 class="title-contact text-uppercase py-4 pl-3">{{ $t('Contact.title') }}</h3>

                <p class="para pl-3">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit dolores nemo ab aperiam repellendus sequi nostrum architecto sunt incidunt consequuntur?</p>
            </div>

            <form name="contact-form"  action="/thanks" method="POST"  netlify netlify-honeypot="bot-field">
                 <input type="hidden" name="form-name" value="contact-form" />
                <div class="row">
                    <div class="col-md-6">
                        <h4 class="title-form">{{ $t('Contact.form1') }}</h4>
                        <input type="text" name="name" class="form-control form-control-lg" placeholder="Allan Sanchez" required>
                    </div>
                    <div class="col-md-6">
                        <h4 class="title-form">{{ $t('Contact.form2') }}</h4>
                        <input type="email" name="email" class="form-control form-control-lg" placeholder="emial@example.com" required>
                    </div>

                </div>
                <div class="row mt-3">
                    <div class="col-sm-12">
                        <h4 class="title-form">{{ $t('Contact.form3') }}</h4>
                        <textarea required name="message" class="form-control form-control-lg" id="exampleFormControlTextarea1" placeholder="Enter your message here" rows="6"></textarea>
                    </div>
                    <!-- <div class="col-sm-12 col-md-7 col-lg-8 mt-5">
                        <div data-netlify-recaptcha="true"></div>
                    </div> -->
                    <div class="col-sm-12  mt-5">
                        <button type="submit" class="btn button primary-button mr-md-0  text-uppercase  float-right">{{ $t('Contact.btn')}}</button>
                    </div>
                </div>
            </form>
            
        </div>
    </section>
</template>

<style >
    .contact{
        /* background: yellow; */
         padding: 8rem 5rem;
    }

    .contact .title-contact{
         color: var(--title-color);
         font: normal bold 49px/60px var(--roboto);
    }
    .title-form{
        color: var(--title-color);
    }
    
    
</style>