
function(test_build FILENAME)
    set(APP ${FILENAME})
    add_executable(${APP} ${FILENAME}.c)
    target_link_libraries(${APP} nativefiledialog)
    install(TARGETS ${APP} RUNTIME DESTINATION bin)
endfunction()

test_build(test_opendialog)
test_build(test_opendialogmultiple)
test_build(test_pickfolder)
test_build(test_savedialog)
