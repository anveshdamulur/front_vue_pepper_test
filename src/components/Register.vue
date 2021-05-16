<template>
    <div class="register">
            <div class="register__container">
                <div class="container__left">
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
                                <form @submit="checkForm" class="signup__form">
                                    <label htmlFor="username" class="label__heading">Username</label>
                                    <input type="text" name="username" v-model="username" placeholder="mail@somedomain.com" />  
                                    <!-- <li v-for="(error, index) in errors" :key="index">{{error}} </li>                                 -->
                                    <label htmlFor="email" class="label__heading">Email</label>
                                    <input type="text" name="email" v-model="email" placeholder="mail@somedomain.com" />
                                    <label htmlFor="password" class="label__heading">Password</label>
                                    <input type="password" v-model="password" placeholder="Min. 8 character" name="password" id="" />
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
                <div class="container__right">
                   
                    <img src="../assets/bg_1_Tavola_disegno_1.jpg" alt="image" srcset="" />

                   
                </div>
            </div>
        </div>
</template>

<script>
export default {
    name : "Register",
    data(){
        return{
            errors : [],
            username : null,
            email : null,
            password : null
        }
    },
    methods : {
        checkForm : function(e){

            this.errors=[];

            if(!this.username){
                this.errors.push("invalid username")
            }

            if(!this.password){
                this.errors.push("invalid pass")
            }

            if(!this.email){
                this.errors.push("invalid email id")
            }
            else if(!this.validEmail(this.email)){
                this.errors.push("valid email is required")
            }

            if(!this.errors.length){
                return true
            }
             e.preventDefault();

        },
        validEmail : function(email){
             var re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
            return re.test(email);
        }
    }
}
</script>

<style scoped>
  
.register{
    max-width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.register__container{
    display: flex;
    width: 100%;
}
.container__left{
    display: flex;
    width: 50%;
    justify-content: center;
    /* margin-top: 16px;
    margin-bottom: 16px; */
    background-color: var(--pink);
    height: 95vh;
}

.register__left__info{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 70%;
    margin-top: 30px;
    margin-left: 120px;
    margin-right: 120px;
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
    height: 34px;
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
    height: 8px;
    padding:18px;
    outline: none;
    background-color:var(--pink) ;
    border: 0.2px solid var(--silver);
    
}
.signup__form .submit{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    border-radius: 50px;
    margin-top: 20px;
    height: 34px;
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

.container__right{
    display: flex;
    width: 50%;
    /* margin-top: 16px;
    margin-bottom: 16px; */
}


.container__right > img{
    width: 100%;
    height: 95vh;
    transform: scaleX(-1);
}
</style>