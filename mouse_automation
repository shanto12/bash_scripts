Write-Host "Started!!!"

'#######################################'

$continue_hours=10

$gap_minutes=3

'#######################################'

 

$waited_seconds = 0

$total_seconds = $continue_hours*60*60

$min_wait =($gap_minutes - ($gap_minutes*.1))*60

$max_wait = ($gap_minutes + ($gap_minutes*.1))*60

 

Write-Host "waited_seconds: $waited_seconds."

Write-Host "total_seconds: $total_seconds."

Write-Host "min_wait: $min_wait."

Write-Host "max_wait: $max_wait."

 

while($waited_seconds -lt $total_seconds)

{

                $wshell = New-Object -ComObject wscript.shell;

                $wshell.AppActivate('mytext.txt')            

                #$wshell.SendKeys('~') 

                $wshell.SendKeys("{LEFT}")        

                $wshell.SendKeys("{RIGHT}")        

                $wait_time = Get-Random -Minimum $min_wait -Maximum $max_wait   

                Write-Host "Sleeping for $wait_time"    

                Start-Sleep -s $wait_time            

                $waited_seconds=$waited_seconds+$wait_time

                Write-Host "Total waited_seconds: $waited_seconds. This wait_time: $wait_time"          

}

Write-Host "Finished!!!"

