---
layout: post
title: How to clean up your Home Assistant database
published: false
---
This one let's you keep your DB in a great shape.

First you need to know that all your beautiful sensor updates takes space in your DB. Then, if running in a raspberry pi with micro SD Card, you should also know that micro SD cards are know for dieing after a number of writes[^1].

So taking those two into consideration, do you really need to save all the times you've opened a window or is it good enough to know the current state? That will depend on your automation but probably there is a ton of info you do not need to keep track off.

In order to deal with all this, you need to know that you cna use recorder integration[^2] to specify what do you want and for how long you want to keep it.

If you want to check what's in the database taking space you can use the SQLite web addon[^] with the following query (thanks to pacienciadigital[^4] blog):

SELECT entity_id, COUNT(*) as count FROM states GROUP BY entity_id ORDER BY count DESC LIMIT 10

Days after you add the stuff you don't want to the recorder, they will be all gone (depending on the purge_keep_days configuration). If you want to speed things up, go to developer tools and check for the purge service, there you should be able to purge specific data.

[^1]:  [One of many threads discussing micro SD wear](https://community.home-assistant.io/t/raspberry-pi-sd-card-wear/335169)
[^2]:  [Recorder integration](https://www.home-assistant.io/integrations/recorder/)
[^3]:  [SQLite web addon](https://github.com/hassio-addons/addon-sqlite-web/blob/main/README.md)
[^4]:  [Cómo optimizar la base de datos sqlite de Home Assistant](https://www.pacienciadigital.com/base-de-datos-sqlite-home-assistant/)