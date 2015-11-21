PROJECT := ${notdir ${PWD}}
BITBAKE  = PATH=$${PATH}:bitbake/bin bitbake ${BBFLAGS}

all:  bitbake ; ${BITBAKE}     ${PROJECT}
bitbake-run:  ; ${BITBAKE}
bitbake-%:    ; ${BITBAKE} -$*
${PROJECT}-%: ; ${BITBAKE} -$* ${PROJECT}
%:            ; ${BITBAKE}  $*

bitbake:
	git clone git://github.com/openembedded/bitbake
	cd bitbake && git checkout -b 1.24 bd9d827

clean:
	rm -rf bitbake bitbake.lock temp
