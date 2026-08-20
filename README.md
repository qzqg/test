# test-jghgfc kjkjkjij
package main

import (
	"fmt"
	"os/exec"
)

func main() {
	cmd := exec.Command(
		`C:\Users\Kh_Sa\Downloads\platform-tools\adb.exe`,
		"shell",
		"echo",
		"hello from phone",
	)

	output, err := cmd.CombinedOutput()
	if err != nil {
		fmt.Println("Error:", err)
		return
	}

	fmt.Print(string(output))
}
