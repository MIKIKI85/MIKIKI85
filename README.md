@echo off
Title Witam w symulatorze komputera

:Logowanie
color 0C
set /p answer=Zaloguj sie do komputera 
if %answer%==MIKIKI goto Pulpit
if not %answer%==MIKIKI goto Logowanie2

:Logowanie2
echo Zla odpowiedz
color 0C
set /p answer=Sprobuj ponownie 
if %answer%==MIKIKI goto Pulpit
if not %answer%==MIKIKI goto Logowanie2

:Pulpit
color 0A
echo.
echo Witaj w pulpicie
echo 1.Zdjecia
echo 2.Notatnik 1
echo 22.Zobaczenie notatnika 1
echo 3.Notatnik 2
echo 33.Zobaczenie 2 notatnika
echo 11.Gry 
set /p "answer=>>"=
if %answer%==1 goto Link_1
if %answer%==2 goto Notatnik_1
if %answer%==22 goto Czytanie_Notatnik_1
if %answer%==3 goto Notatnik_2
if %answer%==33 goto Czytanie_Notatnik_2
if %answer%==11 goto Link_2
pause

:Notatnik_2
set /p "pisanie_2=>>"
set /p answer=kliknij 2 aby wyjsc do pulpitu 
if %answer%==2 goto Pulpit
if not %answer%==2 goto Notatnik_2
pause


:Czytanie_Notatnik_2
echo %pisanie_2%
set /p answer=kliknij 2 aby wyjsc do pulpitu 
if %answer%==2 goto Pulpit
pause

:Link_1
start https://j687gp.webwave.dev/
set /p answer=kliknij 2 aby wyjsc do pulpitu
if %answer%==2 goto Pulpit
if not %answer%==2 goto Exit
pause

:Link_2
start https://www.gry.pl/
set /p answer=kliknij 2 aby wyjsc do pulpitu 
if %answer%==2 goto Pulpit
if not %answer%==2 goto Exit

:Notatnik_1
set /p "pisanie_1=>>"
set /p answer=kliknij 2 aby wyjsc do pulpitu 
if %answer%==2 goto Pulpit
if not %answer%==2 goto Notatnik_1
pause

:Czytanie_Notatnik_1
echo %pisanie_1%
set /p answer=kliknij 2 aby wyjsc do pulpitu 
if %answer%==2 goto Pulpit
if not %answer%==2 goto Czytanie_Notatnik_1
pause


:Exit
cls
exit /b
