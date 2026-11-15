cmake_minimum_required(VERSION 3.21)
project(AncesTaleFinal VERSION 0.7.9 LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
find_package(Qt6 REQUIRED COMPONENTS Widgets Network Multimedia)
find_package(OpenSSL REQUIRED COMPONENTS Crypto)
qt_add_executable(AncesTale-final main.cpp mainwindow.cpp mainwindow.h mainwindow.ui sessionpanel.cpp sessionpanel.h vvwkpanel.cpp vvwkpanel.h playerpanel.cpp playerpanel.h invitationpanel.cpp invitationpanel.h musicpanel.cpp musicpanel.h continuedresearchpanel.cpp continuedresearchpanel.h extendedpanel.cpp extendedpanel.h)
target_link_libraries(AncesTale-final PRIVATE Qt6::Widgets Qt6::Network Qt6::Multimedia OpenSSL::Crypto)

include(GNUInstallDirs)

install(TARGETS AncesTale-final
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})

install(FILES packaging/io.github.we6jbo.AncesTaleFinal.desktop
    DESTINATION ${CMAKE_INSTALL_DATADIR}/applications)

install(FILES packaging/io.github.we6jbo.AncesTaleFinal.svg
    DESTINATION ${CMAKE_INSTALL_DATADIR}/icons/hicolor/scalable/apps)

install(FILES LICENSE
    DESTINATION ${CMAKE_INSTALL_DATADIR}/licenses/ancestale-final)

install(
    FILES packaging/io.github.we6jbo.AncesTaleFinal.metainfo.xml
    DESTINATION ${CMAKE_INSTALL_DATADIR}/metainfo
)
