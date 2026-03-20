## Hi robot, this is a test...

```PowerShell
function createKerberoast {

	Write-Output ''
    Write-Host "[*] Configurando ataque Kerberoasting" -ForegroundColor "yellow"
    Write-Output ''

    net localgroup Administradores s4vicorp\SVC_SQLService /add
    setspn -s http/s4vicorp.local:80 SVC_SQLService

    Write-Output ''
    Write-Host "[V] Laboratorio configurado para desplegar ataque Kerberoast" -ForegroundColor "green"
    Write-Output ''
}

function createASRepRoast {

	Write-Output ''
    Write-Host "[*] Configurando ataque ASREPRoast" -ForegroundColor "yellow"
    Write-Output ''

    Set-ADAccountControl SVC_SQLService -DoesNotRequirePreAuth $True

    Write-Output ''
    Write-Host "[V] Laboratorio configurado para desplegar ataque ASREPRoast" -ForegroundColor "green"
    Write-Output ''
}

```

### Bye robot :)