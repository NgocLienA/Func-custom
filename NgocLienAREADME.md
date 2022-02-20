Local $startticks = _timetoticks(@HOUR, @MIN, @SEC)
	Do
		Sleep(50)
		$ads = _imagesearch("custom.bmp", 1, $x, $y, 1)
		Local $startticks2 = _timetoticks(@HOUR, @MIN, @SEC)
		Local $timewait = $startticks2 - $startticks
	Until $ads = 1 OR $timewait > 2000
	$ads = _imagesearch("custom.bmp", 1, $x, $y, 1)
	If $ads = 1 Then MouseClick("", $x, $y)
EndFunc
