# task

import speech_recognition as sr
a=sr.Recognizer
with sr.Microphone() as source:
    print("speak:")
    audio=a.listen(source)
try:
     text=r.recognize_google(audio)
    print("you said:",text)
except sr.unkownValueError:
    print("could not understand audio")
except sr.RequestError as e:
    print("could not request result;{0}".format(e))
 import abc
intentslist=[('otp','OTP'),('prize','PRIZE'),('luckydraw','LUCKYDRAW'),('account','ACCOUNT'),('lakhs','LAKHS')]
intentunknown=True
for phrase, intent in intentslist:
    if phrase in MyText:
        if intent=='OTP':
            otp=MyText.split(phrase)[1]
            otp=otp.strip()
            print('i have got my',otp)
            intentunknown=False
            break
        elif intent=='PRIZE':
            prize=MyText.split(phrase)[2]
            prize=prize.strip()
            print('i have got my',prize)
            intentunknown=False
            break
        elif intent=="LUCKYDRAW":
            luckydraw=MyText.split(phrase)[3]
            luckydraw=luckydraw.strip()
            print('i have got my',luckydraw)
            intentunknown=False
            break
        elif intent=="ACCOUNT":
            account=MyText.split(phrase)[4]
            account=account.strip()
            print('i have got my',account)
            intentunknown=False
            break
        elif intent=="LAKHS":
            lakhs=MyText.split(phrase)[5]
            lakhs=lakhs.strip()
            print('i have got my',lakhs)
            intentunknown=False
            break
if intentunknown:
    print("you said:",MyText)
    print("i don't known")
