

# SEL0337 — Projetos em Sistemas Embarcados 
## Prática 5: Boot Inicial Placa

**Integrantes:**
* Arthur Palhares Barbieri — N° USP: `15697357`
* Pedro Galvani Cassiano Teixeira — N° USP: `15676072`
* Thalys de Azevedo Leite — N° USP: `15580274`

---


###  Checkpoint 1 — Serviço Embarcado no Boot (`blink_python.service`)
* **`[Unit]`:** Define a descrição exibida no boot e aguarda o alvo `multi-user.target`.
* **`[Service]`:** Executa `/usr/bin/python3 /home/sel/SEL0337-Pratica5/blink_service.py` via `ExecStart` e executa `blink_stop.py` via `ExecStop` para apagar o LED na GPIO 18 e liberar o pino (`GPIO.cleanup()`) ao rodar `sudo systemctl stop blink_python`.
* **`[Install]`:** Habilita o serviço no boot via `sudo systemctl enable blink_python`.
EOF
