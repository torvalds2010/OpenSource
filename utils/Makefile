# Makefile

include ../Make_include

LIBS    += -L$L -lgenfft -lm $(LIBSM)
#OPTC += -openmp 
#OPTC += -g -O0

ALL: makemod makewave extendModel fconv correigen green basop syn2d mat2su ftr1d

SRCM	= \
		makemod.c  \
		wallclock_time.c  \
		diffraction.c \
		randdf.c \
		elipse.c \
		fractint.c \
		grid.c \
		gridabove.c \
		interpolation.c \
		linearint.c \
		plotexample.c \
		polint.c \
		roughint.c \
		sinusint.c \
		spline.c \
		name_ext.c  \
		allocs.c  \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCW	= \
		makewave.c \
		wallclock_time.c \
		freqwave.c \
		allocs.c  \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCE	= \
		extendModel.c \
		wallclock_time.c \
		allocs.c  \
		getModelInfo.c  \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCF	= fconv.c \
		getFileInfo.c  \
		readData.c \
		writeData.c \
		wallclock_time.c \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCC	= correigen.c \
		getFileInfo.c  \
		readData.c \
		writeData.c \
        name_ext.c  \
		wallclock_time.c \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c


SRCG	= green.c \
		getFileInfo.c  \
		getrecpos.c  \
		readData.c \
		writeData.c \
		wallclock_time.c \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCB	= basop.c \
		getFileInfo.c  \
		readData.c \
		writeData.c \
		wallclock_time.c \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCS	= syn2d.c \
		getFileInfo.c  \
		readData.c \
		writeData.c \
		wallclock_time.c \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCA	= mat2su.c \
		wallclock_time.c \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

SRCT	= ftr1d.c \
		getFileInfo.c  \
		readData.c \
		writeData.c \
		wallclock_time.c \
		verbosepkg.c  \
		atopkge.c \
		docpkge.c \
		getpars.c

OBJM	= $(SRCM:%.c=%.o)

makemod:	$(OBJM) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o makemod $(OBJM) $(LIBS)

OBJW	= $(SRCW:%.c=%.o)

makewave:	$(OBJW) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o makewave $(OBJW) $(LIBS)

OBJE	= $(SRCE:%.c=%.o)

extendModel:	$(OBJE) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o extendModel $(OBJE) $(LIBS)

OBJF	= $(SRCF:%.c=%.o)

fconv:	$(OBJF) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o fconv $(OBJF) $(LIBS)

OBJC	= $(SRCC:%.c=%.o)

correigen:	$(OBJC) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o correigen $(OBJC) $(LIBS)

OBJG	= $(SRCG:%.c=%.o)

green:	$(OBJG) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o green $(OBJG) $(LIBS)

OBJB	= $(SRCB:%.c=%.o)

basop:	$(OBJB) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o basop $(OBJB) $(LIBS)

OBJS	= $(SRCS:%.c=%.o)

syn2d:	$(OBJS) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o syn2d $(OBJS) $(LIBS)

OBJA	= $(SRCA:%.c=%.o)

mat2su:	$(OBJA) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o mat2su $(OBJA) $(LIBS)

OBJT	= $(SRCT:%.c=%.o)

ftr1d:	$(OBJT) 
	$(CC) $(LDFLAGS) $(OPTC) $(CFLAGS) -o ftr1d $(OBJT) $(LIBS)

install: makemod makewave extendModel fconv correigen green basop syn2d mat2su ftr1d
	cp makemod $B
	cp makewave $B
	cp extendModel $B
	cp fconv $B
	cp correigen $B
	cp green $B
	cp basop $B
	cp syn2d $B
	cp mat2su $B
	cp ftr1d $B

clean:
		rm -f core $(OBJM) makemod $(OBJW) makewave $(OBJE) extendModel $(OBJF) fconv $(OBJG) $(OBJC) correigen green $(OBJB) basop $(OBJJ) syn2d $(OBJS) mat2su $(OBJA) ftr1d $(OBJT)

realclean: clean
		rm -f $B/makemod $B/makewave $B/extendModel $B/fconv $B/correigen $B/green $B/basop $B/syn2d $B/mat2su $B/ftr1d




