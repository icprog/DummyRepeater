OBJECTS = DummyRepeaterApp.o DummyRepeaterBleepSet.o DummyRepeaterCallsignSet.o DummyRepeaterControllerSet.o DummyRepeaterDongleSet.o \
	  DummyRepeaterErrorEvent.o DummyRepeaterFrame.o DummyRepeaterHeaderEvent.o DummyRepeaterMessageEvent.o DummyRepeaterMessageSet.o \
	  DummyRepeaterNetworkSet.o DummyRepeaterPreferences.o DummyRepeaterSlowDataEvent.o DummyRepeaterSoundcardSet.o \
	  DummyRepeaterStatusEvent.o DummyRepeaterThread.o DummyRepeaterTimeoutSet.o DummyRepeaterTXEvent.o

all:		dummyrepeater

dummyrepeater:	$(OBJECTS)
		$(CXX) $(OBJECTS) ../Common/Common.a $(LDFLAGS) $(LIBS) -o dummyrepeater

%.o: %.cpp
		$(CXX) $(CFLAGS) -I../Common -c -o $@ $<

install:
		install -g bin -o root -m 0775 dummyrepeater $(BINDIR)

clean:
		$(RM) dummyrepeater *.o *.d *.bak *~

