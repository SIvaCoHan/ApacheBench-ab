APR=apr-1.4.6
APRUTIL=apr-util-1.4.1

all:$(APR) $(APRUTIL) buildapr

$(APR):
	wget http://apache.techartifact.com/mirror//apr/$(APR).tar.gz
	tar -xf $(APR).tar.gz
$(APRUTIL):
	wget http://apache.techartifact.com/mirror//apr/$(APRUTIL).tar.gz
	tar -xf $(APRUTIL).tar.gz

buildapr:
	cp Makefile_apr $(APR)
	make -C $(APR) -f Makefile_apr	
	cp Makefile_aprutil $(APRUTIL)
	make -C $(APRUTIL) -f Makefile_aprutil

clean:
	rm -rf apr-*
	rm -rf aprutil-*
	
