beamdir = ../ebin
beam_DATA = cloudi_job_messaging_sequence1.beam \
            cloudi_job_messaging_sequence2.beam \
            cloudi_job_messaging_sequence3.beam
CLEANFILES = $(beam_DATA) \
             $(beamdir)/cloudi_job_messaging_sequence1.beam \
             $(beamdir)/cloudi_job_messaging_sequence2.beam \
             $(beamdir)/cloudi_job_messaging_sequence3.beam

all-local: $(beam_DATA)
	$(MKDIR_P) $(beamdir) || exit 0
	cp -f $(beam_DATA) $(beamdir)

.erl.beam:
	@ERLC@ -b beam -I $(top_srcdir)/lib/cloudi/include \
           -pz $(top_builddir)/lib/cloudi/ebin \
           -o $@ $<
