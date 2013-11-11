#Tutorial3: LOIC++.cpp Flooder.o HTTPFlooder.o XXPFlooder.o 
#	g++ -Wall -o loic++ LOIC++.cpp Flooder.o HTTPFlooder.o XXPFlooder.o -lboost_thread-mt -lboost_date_time -lssl -lcrypto -lboost_program_options
http: LOIC++.cpp Flooder.o HTTPFlooder.o
	g++ -Wall -o test LOIC++.cpp Flooder.o HTTPFlooder.o -std=c++0x -lssl -lcrypto -lboost_program_options
# now define how each object file is a target and list dependencies and how
#  to build that object file if any dependencies change
	
Flooder.o: Flooder.cpp
	g++ -Wall -c Flooder.cpp -std=c++0x


HTTPFlooder.o: Flooder.o HTTPFlooder.h HTTPFlooder.cpp
	g++ -Wall -c HTTPFlooder.cpp -std=c++0x

XXPFlooder.o:	Flooder.o XXPFlooder.h XXPFlooder.cpp
	g++ -Wall -c XXPFlooder.cpp -std=c++0x
	
clean:
	rm  loic++ *.o *.gch test


# that's all

