LIBS=-lpcap -lboost_system -lpcl_registration -lpcl_common -lpcl_kdtree -lpcl_io -lpcl_sample_consensus -lpcl_features -lflann_cpp -lpcl_search
PCL_LIB = -L/usr/lib -lpthread -lm -lstdc++ -lpcl_common -lpcl_io -lpcl_io_ply -lpcl_filters -lm -lpng -lusb-1.0 -lOpenNI -lusb-1.0 -lOpenNI -lpcap -Wl,-rpath,/usr/local/lib
# PCL_LIB = -L/usr/local/lib -lpthread -lm -lstdc++ -lpcl_common -lpcl_io -lpcl_io_ply -lpcl_filters -lm -lpng -lusb-1.0 -lOpenNI -lusb-1.0 -lOpenNI -lpcap -Wl,-rpath,/usr/local/lib
BOOST_LIB = -L/usr/lib/x86_64-linux-gnu -lboost_system -lboost_filesystem  -lboost_thread -lboost_date_time -lboost_iostreams -lboost_system -lboost_filesystem -lboost_thread -lboost_date_time -lboost_iostreams -Wl,-rpath,/opt/local/lib
# BOOST_LIB = -L/usr/lib/x86_64-linux-gnu -lboost_system-mt -lboost_filesystem-mt  -lboost_thread-mt -lboost_date_time-mt -lboost_iostreams-mt -lboost_system-mt -lboost_filesystem-mt -lboost_thread-mt -lboost_date_time-mt -lboost_iostreams-mt -Wl,-rpath,/opt/local/lib
# DON_INC = -I../DoNFilter
HDL_GRABBER = ../MyHdlGrabber/MyHdlGrabber.cpp -I../MyHdlGrabber
PCL_INCLUDE = -I/usr/include/pcl-1.7
EIGEN_INCLUDE = -I/usr/include/eigen3

all:	pcap_dump

pcap_dump:
	g++ PcapDump.cpp $(HDL_GRABBER) $(EIGEN_INCLUDE) $(PCL_INCLUDE) -o pcap_dump.exe -Wall $(LIBS) $(PCL_LIB) $(BOOST_LIB)

clean:
	rm pcap_dump.exe
