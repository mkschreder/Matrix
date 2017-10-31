set(tests
	setIdentity
	inverse
	slice
	matrixMult
	vectorAssignment
	matrixAssignment
	matrixScalarMult
	transpose
	vector
	vector2
	vector3
	attitude
	filter
	integration
	squareMatrix
	quaternion
	helper
	hatvee
	glm_compliance
	)

add_custom_target(test_build)
foreach(test_name ${tests})
	add_executable(${test_name}
		${test_name}.cpp)
	add_test(test_${test_name} ${test_name})
	add_dependencies(test_build ${test_name})
endforeach()

