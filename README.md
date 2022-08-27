# Go dispatch proxy

## QuickStart

An example for 2 connections (Phone & Modem)

### Windows Command-Line

```
cd DIRECTORY
set ip_address_phone="Phone, IP"
set ip_address_modem="Mobilfunk, IP"
for /f "usebackq tokens=2 delims=:" %%f in (`go-dispatch-proxy.exe -list ^| findstr /c:%ip_address_phone%`) do set ip_address_phone=%%f
for /f "usebackq tokens=2 delims=:" %%f in (`go-dispatch-proxy.exe -list ^| findstr /c:%ip_address_modem%`) do set ip_address_modem=%%f
go-dispatch-proxy.exe %ip_address_phone%@1 %ip_address_modem%@2
```

## Normal usage

`go-dispatch-proxy.exe IPADDRESS`

### Available Devices
`go-dispatch-proxy.exe -list`
