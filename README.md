r, c = 1, 1

while True:
    # desenhando o grid 3x3
    for i in range(3):
        linha = ""
        for j in range(3):
            linha += "@" if (i == r and j == c) else "."
            if j < 2: linha += " "
        print(linha)
    print()  # espaço

    cmd = input("Mover (w/a/s/d) ou q para sair: ").strip().lower()
    if cmd == "q":
        print("Falou! 👋")
        break
    if cmd == "w" and r > 0: r -= 1
    elif cmd == "s" and r < 2: r += 1
    elif cmd == "a" and c > 0: c -= 1
    elif cmd == "d" and c < 2: c += 1
    else:
        print("Comando inválido ou movimento impossível.\n")

    # limpa tela simples (apenas para deixar a saída mais limpa)
    print("\n" * 5)
