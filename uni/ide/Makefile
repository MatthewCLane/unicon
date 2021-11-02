# makefile for v2-gui Unicon IDE

BASE=../..
include $(BASE)/Makedefs.uni

# needed to link idol.u
export IPATH:=$(UNI)/unicon

# nothing to configure here yet

UFLAGS=-s -c -u
UFLAGS2=-s -c

SRC=ui.icn ide.icn hfiledialog.icn buffertextlist.icn buffertabset.icn \
	buffertabitem.icn mainbar.icn modified.icn preferences.icn \
	templates.icn definitions.icn uproject.icn \
	classbrowser.icn tree.icn imgs.icn utags.icn matchparen.icn \
	qu_replace.icn online.icn about.icn is_binary.icn ptyDispatcher.icn \
	shelletl.icn funclookup.icn ivib/attribtab.icn ivib/basiccanvascomponentui.icn \
	ivib/buttongroupset.icn ivib/canvas.icn ivib/canvasborder.icn \
	ivib/canvasborderdialog.icn ivib/canvasborderui.icn ivib/canvasbutton.icn \
	ivib/canvasbuttondialog.icn ivib/canvasbuttongroup.icn ivib/canvascheckbox.icn \
	ivib/canvascheckboxdialog.icn ivib/canvascheckboxgroup.icn \
	ivib/canvascheckboxmenuedit.icn ivib/canvascheckboxmenuitem.icn \
	ivib/canvascheckboxui.icn ivib/canvascomponent.icn \
	ivib/canvascomponentdialog.icn ivib/canvascomponentui.icn \
	ivib/canvascustom.icn ivib/canvascustomdialog.icn ivib/canvascustomui.icn \
	ivib/canvaseditabletextlist.icn ivib/canvaseditabletextlistdialog.icn \
	ivib/canvaseditabletextlistui.icn ivib/canvaseditlist.icn \
	ivib/canvaseditlistdialog.icn ivib/canvaseditlistui.icn \
	ivib/canvashscrollbarui.icn ivib/canvasicon.icn ivib/canvasiconbutton.icn \
	ivib/canvasiconbuttondialog.icn ivib/canvasiconbuttonui.icn \
	ivib/canvasicondialog.icn ivib/canvasiconui.icn ivib/canvasimage.icn \
	ivib/canvasimagedialog.icn ivib/canvasimageui.icn ivib/canvaslabel.icn \
	ivib/canvaslabeldialog.icn ivib/canvaslabelui.icn ivib/canvaslist.icn \
	ivib/canvaslistdialog.icn ivib/canvaslistui.icn ivib/canvasmenu.icn \
	ivib/canvasmenubar.icn ivib/canvasmenubardialog.icn ivib/canvasmenubarui.icn \
	ivib/canvasmenubutton.icn ivib/canvasmenubuttonui.icn \
	ivib/canvasmenucomponent.icn ivib/canvasmenucomponentdialog.icn \
	ivib/canvasmenuseparator.icn ivib/canvasmenuseparatoredit.icn \
	ivib/canvasoverlayitem.icn ivib/canvasoverlayset.icn \
	ivib/canvasoverlaysetdialog.icn ivib/canvasoverlaysetui.icn \
	ivib/canvaspanel.icn ivib/canvaspaneldialog.icn ivib/canvaspanelui.icn \
	ivib/canvasscrollbar.icn ivib/canvasscrollbardialog.icn ivib/canvastabitem.icn \
	ivib/canvastable.icn ivib/canvastablecolumn.icn ivib/canvastabledialog.icn \
	ivib/canvastableui.icn ivib/canvastabset.icn ivib/canvastabsetdialog.icn \
	ivib/canvastabsetui.icn ivib/canvastextbutton.icn \
	ivib/canvastextbuttondialog.icn ivib/canvastextbuttonui.icn \
	ivib/canvastextfield.icn ivib/canvastextfielddialog.icn \
	ivib/canvastextfieldui.icn ivib/canvastextlist.icn \
	ivib/canvastextlistdialog.icn ivib/canvastextlistui.icn \
	ivib/canvastextmenuitem.icn ivib/canvastoolbar.icn \
	ivib/canvastoolbardialog ivib/canvastoolbarui.icn ivib/canvasvscrollbarui.icn \
	ivib/cdialog.icn ivib/checkboxgroupset.icn ivib/choicedialog.icn ivib/code.icn \
	ivib/commondialog.icn ivib/componentsort.icn ivib/custom.icn ivib/eventtab.icn \
	ivib/gridelement.icn ivib/gridset.icn ivib/group.icn ivib/groupset.icn \
	ivib/groupsetdialog.icn ivib/hcomponentsort.icn ivib/infodialog.icn \
	ivib/ivibmigrate.icn ivib/main.icn ivib/menucomponentedit.icn ivib/menutree.icn \
	ivib/menutreenode.icn ivib/savechangesdialog.icn ivib/utils.icn \
	ivib/vcomponentsort.icn ivib/version.icn ivib/canvashlineui.icn \
	ivib/canvasline.icn ivib/canvaslinedialog.icn ivib/canvasvlineui.icn \
	ivib/canvastreeui.icn ivib/canvastree.icn ivib/canvastreedialog.icn \
	ivib/canvaslistspinui.icn ivib/canvaslistspin.icn ivib/canvaslistspindialog.icn \
	ivib/canvasrangespinui.icn ivib/canvasrangespin.icn \
	ivib/canvasrangespindialog.icn ivib/canvashsliderui.icn ivib/canvasslider.icn \
	ivib/canvassliderdialog.icn ivib/canvasvsliderui.icn ivib/canvashsizerui.icn \
	ivib/canvassizer.icn ivib/canvassizerdialog.icn ivib/canvasvsizerui.icn\


OBJ=ui.u ide.u hfiledialog.u buffertextlist.u buffertabset.u buffertabitem.u \
	mainbar.u modified.u preferences.u templates.u definitions.u \
	uproject.u classbrowser.u imgs.u utags.u matchparen.u qu_replace.u \
	online.u about.u is_binary.u ptyDispatcher.u shelletl.u funclookup.u\

.PHONY: ivib

all: ivib ui

ivib:
	cd ivib && $(MAKE)

ui:	$(OBJ)
	$(UC) $(DASHG) -o ui $(OBJ)
	$(CP) ui$(EXE) ../../bin

funclookup.u: funclookup.icn
	$(UC) $(UFLAGS) funclookup


ide.u: ide.icn
	$(UC) $(UFLAGS) ide

hfiledialog.u: hfiledialog.icn
	$(UC) $(UFLAGS) hfiledialog

online.u: online.icn
	$(UC) $(UFLAGS) online

about.u: about.icn
	$(UC) $(UFLAGS) about

is_binary.u: is_binary.icn
	$(UC) $(UFLAGS) is_binary

buffertextlist.u: buffertextlist.icn ../gui/editabletextlist.icn
	$(UC) $(UFLAGS) buffertextlist

buffertabitem.u: buffertabitem.icn
	$(UC) $(UFLAGS) buffertabitem

buffertabset.u: buffertabset.icn
	$(UC) $(UFLAGS) buffertabset

matchparen.u: matchparen.icn
	$(UC) $(UFLAGS)  matchparen

preferences.u: preferences.icn
	$(UC) $(UFLAGS)  preferences

mainbar.u: mainbar.icn
	$(UC) $(UFLAGS) mainbar

templates.u: templates.icn
	$(UC) $(UFLAGS) templates

definitions.u: definitions.icn
	$(UC) $(UFLAGS) definitions

uproject.u: uproject.icn
	$(UC) $(UFLAGS) uproject

qu_replace.u: qu_replace.icn
	$(UC) $(UFLAGS) qu_replace

ptyDispatcher.u: ptyDispatcher.icn
	$(UC) $(UFLAGS) ptyDispatcher

shelletl.u: shelletl.icn
	$(UC) $(UFLAGS) shelletl

#idol.u: idol.icn
#	$(UC) $(UFLAGS2) idol

#preproce.u: preproce.icn
#	$(UC) $(UFLAGS2) preproce

#yyerror.u: yyerror.icn
#	$(UC) $(UFLAGS2) yyerror

#unicon.u: unicon.icn
#	$(UC) $(UFLAGS2) unicon

classbrowser.u: classbrowser.icn  imgs.u
	$(UC) $(UFLAGS2) classbrowser

#tree.u: tree.icn
#	$(UC) $(UFLAGS2) tree

utags.u: utags.icn
	$(UC) $(UFLAGS2) utags

ui.u: ui.icn
	$(UC) $(UFLAGS) ui

ui.exe: ui

clean :
	$(RM) *.u uniclass.dir uniclass.pag uniclass.db ui$(EXE)
	cd ivib && $(MAKE) clean
