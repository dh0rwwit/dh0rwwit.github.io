---
title: VBA
author: dh0rwwit
date: 2023-01-29 20:18:00 +0900
categories: [language]
tags: [VBA]
render_with_liquid: false
---

Sub Mergedcells()
	Dim Int_E1Rowcnt as Long
	Dim Int_E2Rowcnt as Long
	Dim Int_E3Rowcnt as Long
	

	For i = 1 To 500
		ActiveSheet.Cell(i,"A").MergeCells.Address
		'ActiveSheet.Cells(i,"B").Value=ActiveSheet.Cells(i,"A").MergeCells
		ActiveSheet.Cells(i,"C").Value=ActiveSheet.Cells(i,"A").MergeArea.Cells(1,1).Value'병합된 셀주소의 값을 대입
		
		If ActiveSheet.Cells(i,"A").MergeArea.Cells(1,1).Value="E1" Then
			Int_E1Rowcnt=Int_E1Rowcnt+1
		End If
		
		If ActiveSheet.Cells(i,"A").MergeArea.Cells(1,1).Value="E2" Then
			Int_E2Rowcnt=Int_E2Rowcnt+1
		End If
		
		If ActiveSheet.Cells(i,"A").MergeArea.Cells(1,1).Value="E3" Then
			Int_E3Rowcnt=Int_E3Rowcnt+1
		End If
	Next i
	
	MsgBox("E1, " & Int_E1Rowcnt)
	MsgBox("E2, " & Int_E2Rowcnt)
	MsgBox("E3, " & Int_E3Rowcnt)
	
'	MsgBox(ActiveSheet.Cells(6,"A").MergeArea.Cells(1,1).Value)
	
End Sub

Sub CurrentRegion()
	Range("C4").CurrentRegion.Select  'C4에서 ctrl+a'

End Sub
