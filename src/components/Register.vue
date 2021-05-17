<template>
    <div class="register">
            <div class="register__container">
                <div class="register__container__left">
                    <div class="register__left__info">
                        <div class="register__logo">
                            <img src="../assets/Pepper_logo_horizontal.png" alt="logo" />
                        </div>
                        <div class="register__signup">
                            <div class="signup__heading">
                                <span>Sign Up</span>
                                <p>Welcome to the club!</p>
                            </div>
                            <div class="signup__google">
                               <img src="../assets/google-logo-icon-png-transparent-background.png" alt="" />
                               <span>Sign up with Google</span>
                            </div>

                            <h6><span>or create an account</span></h6>
                           
                            
                            <div class="signup__container">
                                <form @submit="checkForm" class="signup__form" >            
                                    <label class="label__heading">Username</label>
                                    <input type="text" name="username" v-model="username" placeholder="mail@somedomain.com"/>
                                    <!-- <span class="test_danger" v-if="!$v.username.required && !$v.username.$dirty">Name is required</span>   
                                    <span class="test_danger" v-if="!$v.username.alpha && !$v.username.$dirty">Name is required</span>      -->
                                   

                                    <label class="label__heading">Email</label>
                                    <input type="email" name="email" v-model="email" placeholder="mail@somedomain.com" />
                                    <!-- <span class="test_danger" v-if="(!$v.email.required || !$v.email.email ) && !$v.username.$dirty">Name is required</span>    -->

                                    <label class="label__heading">Password</label>
                                    <input type="password" v-model="password" placeholder="Min. 8 character" name="password" id="" />
                                    <!-- <span class="test_danger" v-if="!$v.password.required  && !$v.password.$dirty">Password is required</span>   
                                    <span class="test_danger" v-if="(!$v.password.minLength || !$v.password.maxLength)  && !$v.password.$dirty">Password must be {{$v.password.$params.minLength.min}} characters!</span>    -->

                                    <input type="submit" class="submit" value="Sign up"/>  
                                </form>
                                <div class="signup__footer">
                                    <p>Already registered?</p>
                                    <span>Sign in</span>
                                </div>
                            </div>
                        </div>
                        
                    </div>
                </div>
                <div class="register__container__right">
                    <img src="../assets/bg_1_Tavola_disegno_1.jpg" alt="image" srcset="" />
                </div>
            </div>
        </div>
</template>

<script>

export default {
    name : "Register",
    data:()=>({

            username : "",
            email : "",
            password : ""
        
    }),
    
}
</script>

<style scoped>
  
.register{
    max-width: 100%;
    max-height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.register__container{
    display: flex;
    width: 100%;
    height: 100%;
}
.register__container__left{
    display: flex;
    width: 50%;
    justify-content: center;
    /* margin-top: 16px;
    margin-bottom: 16px; */
    background-color: var(--pink);
    height: 100vh;
}

.register__left__info{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    height: 100%;
    margin-top: 30px;
    margin-left: 130px;
    margin-right: 160px;
}
.register__logo{
    width: 100%;
    margin-bottom: 20px;
}

.register__logo > img{
    width: 90px;
    margin-left: -20px;
    object-fit: contain;
}



.register__signup{
    display: flex;
    flex-direction: column;
    width: 100%;
}

/* .register__signup> img{
    width: 20px;
} */

.register__signup .signup__heading{
    width: 100%;
    margin-bottom: 30px;
}

.signup__heading > span{
    font-size: 27px;
    font-weight: 900;
    color: var(--black);
}
.signup__heading > p{
    font-size: 17px;
    font-weight: 200;
    margin-top: 10px;
    color: var(--black);

}

.signup__google{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 40px;
    border: 2px solid var(--silver);
    border-radius: 50px;
    cursor: pointer;
    outline: none;
    border: 1px solid var(--silver);
    margin-bottom: 30px;
}

.signup__google > img{
    width: 50px;
    height: 20px;
    object-fit: contain;
}
.signup__google > span{
    font-weight: 400;
    font-size: 11px;
    color: var(--black);

}

h6 {
    width: 100%; 
    text-align: center; 
    border-bottom: 0.1px solid var(--silver); 
    font-weight: 100;
    font-size: 10px;
    line-height: 0.1em;
    color: var(--black);
    margin: 10px 0 20px; 
 }
 h6 >span { 
    background:var(--pink); 
    padding:0 10px; 
    color: var(--silver);
}

.signup__container{
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 400px;

}

.signup__form{
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 300px;
    margin-top: 10px;
}

.signup__form > label{
    width: 100%;
    font-size: 11px;
    font-weight: 400;
    margin-top: 10px;
    margin-bottom: 3px;
    color: var(--black);

}
.signup__form > input{
    border-radius: 50px;
    width: 100%;
    height: 40px;
    padding:18px;
    outline: none;
    background-color:var(--pink) ;
    border: 0.2px solid var(--silver);   
}

input[type=submit] {
    padding:5px 15px; 
    background:#ccc; 
    border:0 none;
    cursor:pointer;
    -webkit-border-radius: 5px;
    border-radius: 5px; 
}

::placeholder{
    font-weight: 50;
    font-size: 11px;
    color: var(--silver);
  
}
.signup__form .submit{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    border-radius: 50px;
    margin-top: 20px;
    height: 40px;
    cursor: pointer;
    outline: none;
    border:none;
    background-color: var(--orange);
    color: white;
}

.signup__footer{
    display: flex;
    width: 100%;
    margin-top: -25px;
}
.signup__footer > p{
    font-size: 11px;
    font-weight: 400;
    color: var(--black);

}
.signup__footer > span{
    font-size: 11px;
    margin-left: 3px;
    font-size: 400;
    color: var(--orange);
    cursor: pointer;
}

.register__container__right{
    display: flex;
    width: 50%;
    height: 100vh;
    /* margin-top: 16px;
    margin-bottom: 16px; */
}


.register__container__right > img{
    width: 100%;
    height: 100%;
    transform: scaleX(-1);
}

@media (min-width :1000px)  { 
      .register{
            max-width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
}
@media (max-device-width: 800px) {
    .register{
            max-width: 100%;
            display: flex;
            background-color:var(--pink) ;

        }
        .register__container{
            display: flex;
            flex-direction: column-reverse;
            width: 100%;
            height: 100%;
        }
        .register__logo{
            width: 100%;
            height: 40%;
            margin-bottom: 20px;
            position: relative;
        }

        .register__logo > img{
            width: 90px;
            margin-left: -20px;
            object-fit: contain;
            top: -100px;
        }
        .register__container__left{
            display: flex;
            width: 100%;
            height: 60%;
            justify-content: center;
            background-color: var(--pink);
        }
        .register__left__info{
            display: flex;
            flex-direction: column;
            align-items: center;
           margin: 25px;
            
         
        }
        .register__container__right{
                width: 100%;
                height: 30%;
                position: relative;
                transform: scaleX(-1);
        }
        .register__container__right > img{
            width: 100%;
            height: 500px;
            border-top-left-radius:0;
            border-top-right-radius:0;
            border-bottom-left-radius:50% 20%;
            border-bottom-right-radius: 10% 50% 20%;
        }
}
@media (max-device-width: 400px) {
      .register{
            max-width: 100%;
            background-color:var(--pink) ;
        }
           .register__container__left{
            display: flex;
            width: 100%;
            height: 100%;
            background-color: var(--pink);
        }
          .register__left__info{
            display: flex;
            margin: 20px;
            width: 100%;
            height: 100%;
         
        }
        
}

</style>