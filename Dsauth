var express = require('express');
var app = express();
const config = require('./config.json')
var bodyParser = require('body-parser');
const fetch = require('node-fetch');
const FormData = require('form-data');
const db = require('quick.db')
const mongoose = require('mongoose')
let format = ['png','gif']
mongoose.connect(process.env.mongodb,{
useNewUrlParser: true,
	useUnifiedTopology: true
}).then(() => {
	console.log('connected')
}).catch((err) => {
	console.log('unable connect')
})

const canvas = require('canvas')
const axios = require("axios")

app.use(bodyParser.text());
const token = 'yourtoken'

const loginurl = 'https://discord.com/api/oauth2/authorize?client_id=919883508590207039&redirect_uri=https%3A%2F%2Fapi.emurbot.xyz%2Flogin&response_type=code&scope=identify'

app.get('/', function (req, res) {
res.redirect(loginurl)

/// access token:

app.get('/user/:id', async function (req, res) {
let id = req.params.id.split(".")[0]
const token = process.env.token
	 
		 
	const config = {
                headers:{
                    "authorization":`Bot ${token}`
                }
            }
            axios
                .get(`https://discord.com/api/v9/users/${id}`,config)
                .then(async response=>{
                console.log(response.data)	 
	res.send(`
Username : ${response.data.username}

Id : ${response.data.id}

`)

						
								})
                .catch(error=>{
                    console.log(error)
                })

											

})
				
											
											
							
																		 

app.get('/login', async function (req, res) { 
	
const { url } = require('inspector'); const { URLSearchParams } = require('url');

				var code = req.query.code; 
	
	
	if(!code) return res.redirect(loginurl)
				const params = new URLSearchParams(); params.append('client_id', 'Bot Client id'); params.append('client_secret', 'Bot Secert id '); params.append('grant_type', 'authorization_code'); params.append('code', code); params.append('redirect_uri', 'https://your-domain/login'); 
	params.append('scope', 'identify'); 


	
				var site = await fetch("https://discord.com/api/v9/oauth2/token", { method: 'POST', body: params, headers: {'Content-Type': 'application/x-www-form-urlencoded'}, })

        .then(response => response.json())
        .then(data=>{
            console.log(data)
            const config = {
                headers:{
                    "authorization":`Bearer ${data.access_token}`
                }
            }
            axios
                .get(`https://discord.com/api/v9/users/@me`,config)
                .then(async response=>{
                console.log(response.data)
									
									const { Webhook, MessageBuilder } = require('discord-webhook-node');


    

res.send(`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Discord Auth</title>
    <link rel="icon" href="https://cdn.discordapp.com/attachments/876783877694308392/936906368483463188/Picsart_22-01-29_11-50-25-306.png">
    <meta name="theme-color" content="#014dffde">
    <meta name="og:title" content="EmurBot">
    <meta name="description" content="Emur Is a Bot They Have Moderation And Fun Commands">
    <meta name="og:url" content="https://www.emurbot.xyz/">
    <meta name="og:description" content="Emur Is a Bot They Have Moderation And Fun Commands">
    <meta name="twitter:card" content="summary">
    <meta name="og:image" content="https://cdn.discordapp.com/avatars/919883508590207039/135d3a0ada19263206874ca20ec2ab93.png?size=1024">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Amiri&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.7.2/font/bootstrap-icons.css">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="css/min.css" rel="stylesheet">
    <link href="css/mian.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Amiri&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/waypoints/4.0.1/jquery.waypoints.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Counter-Up/1.0.0/jquery.counterup.min.js"></script>
    <script src="https://unpkg.com/discord-fetcher@1.0.3/index.min.js"></script> 
<section class="py-5" id="about-us">
    <div class="container">
        <h2 class="text-center mb-4 text-info title">User Info</h2>
        <div class="row text-center row-cols-1 row-cols-md-2 g-4 justify-content-center align-items-center">
            <div class="col-sm">
                <div class="card text-light mb-3 card-1">
                    <div class="team-4"></div>
                    <div class="team-5">
                    </div>
                    <div class="h1 mt-3 icon-1">
                        <img src id="avatar-1" style="border-radius: 50%">
                    </div>
                    <div class="card-body text-center">
                        <h4 class="card-title text-info"><strong id="username-1"></strong></h4>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>


<!== ==>
  <script>
function closeNav() {
  document.getElementById("menu-slide").style.width = "0%";
}
async function user_1() {
            let user = await DiscordFetcher("${response.data.id}", {
                dynamic: true,
                size: 1024,
                format: "gif",
                format: "png",
                log: false,
            });
    document.getElementById("avatar-1").src = 'https://cdn.discordapp.com/avatars/${response.data.id}/${response.data.avatar}.webp'        
            document.getElementById("username-1").innerHTML = '${response.data.username}#${response.data.discriminator}'
        }
user_1();
</script>
  

`)


                
								

								})
                .catch(error=>{
                    console.log(error)
                })
																		 })
})

app.listen(8081)
