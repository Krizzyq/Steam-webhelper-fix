# Steam-webhelper-fix

Steam Starting without window 


close steam with task manager

open cmd as admin 

copy paste the command 

change the location to your STEAM ROOT FOLDER

now it should open normaly 



for %D in (bin clientui resource package public tenfoot depotcache) do (
  icacls "A:\steam\%D" /grant "*S-1-15-2-1:(OI)(CI)(RX)" /T
  icacls "A:\steam\%D" /grant "*S-1-15-2-2:(OI)(CI)(RX)" /T
)
icacls "A:\steam\*.exe" /grant "*S-1-15-2-1:(RX)" "*S-1-15-2-2:(RX)"
icacls "A:\steam\*.dll" /grant "*S-1-15-2-1:(RX)" "*S-1-15-2-2:(RX)"
