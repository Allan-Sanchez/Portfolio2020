<template>
    <section class="formulario">
        <div class="container contact">
            <div class="row">
                <h3 class="title-contact">Contact me.</h3>

                <p class="para">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit dolores nemo ab aperiam repellendus sequi nostrum architecto sunt incidunt consequuntur?</p>
            </div>
            <div class="row">
                <div class="col-md-6">
                    <h4 class="title-form">Name</h4>
                    <input type="text" class="form-control form-control-lg" placeholder="Allan Sanchez">
                </div>
                <div class="col-md-6">
                    <h4 class="title-form">Email</h4>
                    <input type="email" class="form-control form-control-lg" placeholder="emial@example.com">
                </div>
                
            </div>
            <div class="row mt-3">
                <div class="col-sm-12">
                    <h4 class="title-form">Message</h4>
                    <textarea class="form-control form-control-lg" id="exampleFormControlTextarea1" placeholder="Enter your message here" rows="6"></textarea>
                </div>
                <div class="col-sm-12  float-right mt-5">
                    <button type="button" class="btn button primary-button mr-md-0 mr-lg-4 text-uppercase">Submit</button>
                </div>
            </div>
            
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