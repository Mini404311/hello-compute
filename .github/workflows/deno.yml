const TelegramBot = require('node-telegram-bot-api');
const bot = new TelegramBot('7868821401:AAEjomsl0i8GEfigrdwL1-MRSvhe8cqw_hk', {polling: true});

// نصائح احترافية للعب روبلوكس
const tips = [
  "🎮 **نصيحة 1**: استخدم زر 'Shift' للجري بسرعة!",
  "💡 **نصيحة 2**: جرب ألعاب 'Obby' لتحسين مهاراتك في القفز.",
  "💰 **نصيحة 3**: لا تشتري 'Robux' إلا من الموقع الرسمي لتجنب الاحتيال.",
  "🏆 **نصيحة 4**: شارك في مسابقات Roblox الرسمية لربح جوائز."
];

// عند إرسال /start
bot.onText(/\/start/, (msg) => {
  const chatId = msg.chat.id;
  bot.sendMessage(
    chatId,
    `مرحباً ${msg.from.first_name}! 👾\n\n` +
    "أنا بوت مساعد لتعلم *اللعب الاحترافي في Roblox*.\n\n" +
    "✅ الأوامر المتاحة:\n" +
    "/tips - نصائح احترافية\n" +
    "/safety - نصائح أمان\n" +
    "/help - المساعدة",
    {parse_mode: "Markdown"}
  );
});

// عند إرسال /tips
bot.onText(/\/tips/, (msg) => {
  const randomTip = tips[Math.floor(Math.random() * tips.length)];
  bot.sendMessage(msg.chat.id, randomTip);
});

// عند إرسال /safety
bot.onText(/\/safety/, (msg) => {
  bot.sendMessage(
    msg.chat.id,
    "🔒 **نصائح أمان مهمة**:\n" +
    "- لا تشارك معلومات حسابك مع أحد\n" +
    "- فعّل التحقق بخطوتين (2FA)\n" +
    "- احذر من مواقع 'Robux المجاني' فهي احتيال",
    {parse_mode: "Markdown"}
  );
});

console.log("✅ البوت يعمل! أرسل /start في Telegram");
