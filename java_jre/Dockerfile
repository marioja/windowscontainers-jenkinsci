# escape=`
FROM microsoft/windowsservercore

RUN powershell -Command `
    wget 'http://javadl.oracle.com/webapps/download/AutoDL?BundleId=234474_96a7b8442fe848ef90c96a2fad6ed6d1' -Outfile 'C:\jreinstaller.exe' ; `
    Start-Process -filepath C:\jreinstaller.exe -passthru -wait -argumentlist "/s,INSTALLDIR=c:\Java\jre1.8.0_181" ; `
    del C:\jreinstaller.exe

ENV JAVA_HOME c:\\Java\\jre1.8.0_181
RUN setx PATH "%PATH%;%JAVA_HOME%\bin"

CMD [ "java.exe" ]
